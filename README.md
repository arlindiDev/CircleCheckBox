# CircleCheckBox
CircleCheckBox is an Android custom view, that simply animates the check.

![](https://media.giphy.com/media/xT0BKuTknR59TZEQjC/giphy.gif)
Download
--------
For now you'll have to manually add the CircleCheckBox.java and ccb_attrs.xml files to your android project, until I add the library to JCenter.


How to use CircleCheckBox?
--------

XML
--------
```xml
<com.arlinddev.CircleCheckBox
    android:id="@+id/chbx"
    android:layout_width="match_parent"
    android:layout_height="60dp"
    android:paddingLeft="5dp"
    app:borderThickness="2dp"
    app:circleBorderColor="#00CFAD"
    app:innerCircleColor="#00CFAD"
    app:innerCircleRadius="14dp"
    app:outerCircleColor="#6400CFAD"
    app:outerCircleRadius="6dp"
    app:showOuterCircle="true"
    app:textColor="#000000"
    app:textLeftPadding="5dp"
    app:textSize="16dp"
    app:tickColor="#ffffff"
    app:tickThickness="1dp"
    app:text="Are you crazy?" />
```
JAVA
--------
```java
protected void onCreate(Bundle savedInstanceState) {
  super.onCreate(savedInstanceState);
  setContentView(R.layout.activity_main);
  CircleCheckBox checkBox = new CheckBox(context);
	checkBox.setOnCheckedChangeListener(new CircleCheckBox.OnCheckedChangeListener() {
	    @Override
	    public void onCheckedChanged(CircleCheckBox view, boolean isChecked) {
	        System.out.println("CHECK "+isChecked);
	    }
	});
} 
```
Public methods
--------
```java
setTickColor(int);
setTickColorHex(String);
setTextColor(int);
setTextColorHex(String);
setShowOuterCircle(boolean);
setInnerCircleColor(int);
setInnerCircleColorHex(String);
setOuterCircleColor(int);
setOuterCircleColorHex(String);
setCircleBorderColor(int);
setCircleBorderColorHex(String);
setTickThickness(float);
setBorderThickness(float);
setTextLeftPadding(float);
setTextSize(float);
setInnerCircleRadius(float);
setOuterCircleRadius(float);
setChecked(boolean);
setText(String);
```
License
--------
This library is licensed under the [The MIT License (MIT)](https://opensource.org/licenses/MIT).
```
  Copyright (c) 2016 Arlind Hajredinaj

  Permission is hereby granted, free of charge,
  to any person obtaining a copy of this software and associated documentation files (the "Software"),
  to deal in the Software without restriction,
  including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense,
  and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so,
  subject to the following conditions:

  The above copyright notice and this permission notice shall be
  included in all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
  EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
  IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
  DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
  <tabTrigger>readme</tabTrigger>
  
  Issues
--------
- Change the Timer to a Handler because of OutOfMemoryException
- Add multiline text



[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-CircleCheckBox-green.svg?style=true)](https://android-arsenal.com/details/1/3746)
