# canvas

    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');

默认的canvas元素是300*150,不设置会让图形被裁切。

    <canvas id="canvas" width="300" height="300"></canvas>
    //or
    canvas.height = 300;
    canvas.width = 300;

    ctx.
        fillRect(x,y,w,h)//填充一个矩形

        stokeRect(x,y,w,h)//绘制一个矩形边框

        strokeRect(x,y,w,h)//清除一个矩形

        moveTo(x,y)//画笔到某个位置

        lineTo(x,y)//画线到某处

        beginPath()//开始路径

        colsePath()//关闭路径

        stroke()//绘制某路径边框

        ctx.strokeStyle = color //设置边框颜色

        fill()//填充某闭合路径,不闭合就无效果 'evenodd'参数为填充两个闭合路径形成的封闭图形,默认'nonzero'

        ctx.fillStyle = color // 设置填充颜色

        arc(x,y,radius,startAngle,endAngle,anticlockwise) // anticlockwise 默认顺时针方向

        createLinearGradient(x1,y1 ,x2 ,y2); //添加渐变
            .addColorStop(position, color);

        createRadialGradient(x1, y1, r1, x2, y2, r2);//添加渐变

        shadowOffsetX = float // 阴影偏移

        shadowOffsetY = float // 阴影偏移

        shadowBlur = float // 阴影模糊度

        shadowColor = color // 阴影色

        fillText(str, x, y, MaxWidth = auto) // MaxWidth可选

        strokeText(str, x, y, MaxWidth = auto) // 绘制文本框

        font = '10px sans-serif' //默认 大小，字体

        textAlign = ['center, start, end, left, right']

        textBaseLine = ['top, hanging, middle, alphabetic, ideographic, bottom'] //alphabetic默认值

        direction = ['ltr, rtl, inherit']

        meausureText() //获得文本的宽度，所在像素

        drawImage(img, x, y, w, h);
        drawImage(img, sx, sy, sw, sh, dx, dy, dw, dh) // 把img中，从sx,sy裁切一sw,sh的矩形，放置到画布dx,dy处大小为dw,dh

        save()

        restore()

        translate(x, y)

        rotate(angle)
        // 这个方法只接受一个参数：旋转的角度(angle)，它是顺时针方向的，以弧度为单位的值。
        // 旋转的中心点始终是 canvas 的原点，如果要改变它，我们需要用到 translate 方法。

        scale(x,y)

        transforms(m11, m12, m21, m22, dx, dy)

        globalCompositeOperation
