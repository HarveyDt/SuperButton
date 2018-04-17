# SuperButton
superbutton
 SuperButton可以实现shape大部分属性设置，减少xml文件，增加开发效率
 
 SuperButton所有属性均提供代码动态设置

      /**
         * 所有属性均可用代码动态实现
         * 以下只是展示部分方法 可根据需求选择不同的方法
         */
        superButton.setShapeType(SuperButton.RECTANGLE)
                .setShapeCornersRadius(20)
                .setShapeSolidColor(getResources().getColor(R.color.colorAccent))
                .setShapeStrokeColor(getResources().getColor(R.color.colorPrimary))
                .setShapeStrokeWidth(1)
                .setShapeSrokeDashWidth(2)
                .setShapeStrokeDashGap(5)
                .setTextGravity(SuperButton.TEXT_GRAVITY_RIGHT)
                .setShapeUseSelector(true)
                .setShapeSelectorPressedColor(getResources().getColor(R.color.gray))
                .setShapeSelectorNormalColor(getResources().getColor(R.color.red_btn))
                .setShapeSelectorDisableColor(getResources().getColor(R.color.colorPrimary))
                .setUseShape();
        // 动态设置切记需要在最后调用 setUseShape 才能对设置的参数生效

布局中如何使用(只是列出部分属性)

           <com.harvey.view.SuperButton
                android:layout_width="70dp"
                android:layout_height="70dp"
                android:layout_margin="5dp"
                android:text="圆角边框"
                stv:sCornersRadius="5dp"
                stv:sStrokeColor="@color/colorAccent"
                stv:sStrokeWidth="0.2dp" />

属性说明(以下属性全部可以通过xml文件配置)

          <?xml version="1.0" encoding="utf-8"?>
          <shape
              xmlns:android="http://schemas.android.com/apk/res/android"
              android:shape=["rectangle" | "oval" | "line" | "ring"] >
              <corners
                  android:radius="integer"
                  android:topLeftRadius="integer"
                  android:topRightRadius="integer"
                  android:bottomLeftRadius="integer"
                  android:bottomRightRadius="integer" />
             <gradient
                  android:angle="integer"
                  android:centerX="integer"
                  android:centerY="integer"
                  android:centerColor="integer"
                  android:endColor="color"
                  android:gradientRadius="integer"
                  android:startColor="color"
                  android:type=["linear" | "radial" | "sweep"]
                  android:useLevel=["true" | "false"] />
             <size
                  android:width="integer"
                  android:height="integer" />
            <solid
                  android:color="color" />
            <stroke
                  android:width="integer"
                  android:color="color"
                  android:dashWidth="integer"
                  android:dashGap="integer" />
          </shape>
