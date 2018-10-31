# SimpleTransparentToolbar

How to implement Transparent ToolBar ::


Step : 1 

First You have to add a library for implementing this . 
I am Using "Kelin-Hong/TranslucentBar"

 implementation 'com.kelin.translucentbar:library:0.8.0'

then Sync your project ...

Step 2:
Open your Value>>Style.XML file 

In your App theme by default if should be 
name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar"

Change it to - > 
name="AppTheme"  parent="Theme.AppCompat.Light.NoActionBar"


After that ... in Styles file add another Custom theme 
I am naming it as AppThemeNO

  <style name="AppThemeNO" parent="Theme.AppCompat.Light.NoActionBar">
  
       <!-- Customize your theme here. -->
  
  <item name="colorPrimary"> @color/colorPrimary</item>
  
  <item name="windowActionBar">false</item>
	
  
        <!-- This two lines are important for this theme here. -->
 
 <item name="windowNoTitle">true</item>
 
 <item name="android:windowTranslucentStatus">true</item>
 <!--  -->
 <item name="colorPrimaryDark"> @color/colorPrimaryDark</item>
 
 <item name="colorAccent">@color/colorAccent</item>
 
 </style>


make the style parent NoActionBar (This is important)


----> See The difference ???

Step 3 :

Now , Work with your  Layout.XML file .

Add AppBarLayout

include your toolbar Layout .


and that's all what you need to make your toolbar transparent 

but if you want your AppBar to have some padding on top . 

then add another layout as parent of your AppBarlayout and then add margine to your

AppBarLayout


So , here is our transparent Toolbar . if you ran it on your phone you will see the 

actual result ..


and do not use |  android:fitsSystemWindows="true" | in your XML 

Thank you ...
few more link :: 
https://stackoverflow.com/questions/29311078/android-completely-transparent-status-bar
