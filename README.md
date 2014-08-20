GlobalCheckBoxPreference
========================

Android's checkbox preference that is customisable and can be used any where like a normal view

##Using GlobalCheckBoxPreference 

###Imports and code changes
* Import the following files to your project(copy+paste)
  * "GlobalCheckBoxPreference.java" to your project package
  * "gobal_check_box_preference.xml" to res/layout/

* Create 'res/values/attrs.xml' and paste the following code
  ```xml
  <?xml version="1.0" encoding="utf-8"?>
  <resources>
      <declare-styleable name="GlobalCheckBoxPreference">
          <attr name="name" format="string" />
          <attr name="summary" format="string" />
          <attr name="summaryOn" format="string" />
          <attr name="summaryOff" format="string" />
          <attr name="defaultValue" format="boolean" />
          <attr name="useSharedPrefs" format="boolean" />
          <attr name="key" format="string" />
      </declare-styleable>
  </resources>
  ```
* Change the following line in GlobalCheckBoxPreference.java(line 3)

  ```java
  import com.manidesto.globalcheckboxprefdemo.R;
  ``` 
  to
  ```java
  import YOUR_APPLICATION_PACKAGE_NAME.R;
  ```
###Understanding attributes
* **name** : Name of the setting or preference
* **summary** : Summary of the setting which is below the name
* **summaryOn** : Summary of the setting when the checkbox is checked
* **summaryOff** : Summary of the setting when the checkbox is unchecked
* **defaultValue** : Default state of the chechbox(checked or unchecked)
* **useSharedPrefs** : Use shared preferences to store the checkbox state. When true the state of the checkbox is retained even if the app is closed

###Using the view
* In the layout file that you want to add the GlobalChechBoxPreference view
  * add
  ```xml
  xmlns:custom="http://schemas.android.com/apk/res/YOUR_APPLICATION_PACKAGE_NAME"
  <!-- YOUR_APPLICATION_PACKAGE_NAME  is the one you write in AndroidManifest.xml -->
  ``` 
  after
  ```xml
  xmlns:android="http://schemas.android.com/apk/res/android"
  ```
  
  * use the view
  ```xml
  <PACKAGE_NAME.GlobalCheckBoxPreference
        custom:name="@string/preference_name"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        custom:defaultValue="true"
        custom:summaryOff="@string/preference_summary_off"
        custom:summaryOn="@string/preference_summary_on"
        custom:useSharedPrefs="false" />
  <!-- PACKAGE_NAME is package name of the package which contains GlobalCheckBoxPreference.java -->
  ```



