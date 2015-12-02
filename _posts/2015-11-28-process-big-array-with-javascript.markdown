---
layout: post
title:  "process big array with javascript"
date:   2015-11-28 14:44:38
categories: javascript array
---


```function process( arr, step, end, index ){
    var startTime = + new Date;
    var len = arr.length;
    index = index || 0;
    while( + new Date - startTime < 30 ){
        if( index == len ){
            end && end();
            return;
        }
        step && step( index, arr[ index ] );
        index++;
    }
    var callee = arguments.callee;
    setTimeout(function(){
        callee( arr, step, end, index );
    }, 0);
}
```

