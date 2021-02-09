
## 遥控杆方向控件

参考大神的项目：https://github.com/luoyexk/JoystickRocker
做了一点小小的改动

# JoystickRocker
这是一个使用Framelayout制作的摇杆控制器自定义控件。在xml中直接使用，目前版本需要提供大圆作为背景图片

![](https://github.com/luoyexk/JoystickRocker/blob/master/image/joystick-demo2.gif)

使用：
<com.zwl9517hotmail.joysticklibrary.CircleViewByImage
        android:id="@+id/joystick_view"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="bottom|right"
        app:background="@drawable/playview_platform_transverse_handle_normal"
        app:foreground="@drawable/control_foreground" />



circleViewByImage.setCallback(callback);


private CircleViewByImage.ActionCallback callback = new CircleViewByImage.ActionCallback() {
        @Override
        public void forwardMove() {
            showAction("up");

        }

        @Override
        public void backMove() {
            showAction("down");
        }

        @Override
        public void leftMove() {
            showAction("left");
        }

        @Override
        public void rightMove() {
            showAction("right");
        }

        @Override
        public void centerMove() {
            showAction("Move a little in center area");

        }

        @Override
        public void centerClick() {
            showAction("Click on center area");
        }

        @Override
        public void actionUp() {
            showAction("action up");

        }
    };