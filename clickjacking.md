# Idea
```
<style>
    iframe {
        position:relative;
        width:$width_value;
        height: $height_value;
        opacity: $opacity;
        z-index: 2;
    }
    div {
        position:absolute;
        top:$top_value;
        left:$side_value;
        z-index: 1;
    }
</style>
<div>Test me</div>
<iframe src=""></iframe>
```
- Change the location of the div to make it on top of the button load by iframe.
- Stupid victim click to div but in fact he click the buton load by iframe.
