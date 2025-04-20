#pr2(login form student registration)
XML (activity_main.xml):

------------------------

<LinearLayout 

 xmlns:android="http://schemas.android.com/apk/res/android"
 android:orientation="vertical"

 android:layout_width="match_parent"

 android:layout_height="match_parent"

 android:padding="16dp"

 android:gravity="center">

 <EditText android:id="@+id/etUser" android:layout_width="match_parent"

 android:layout_height="wrap_content" android:hint="Enter Username" />

 <EditText android:id="@+id/etPass" android:layout_width="match_parent"

 android:layout_height="wrap_content" android:hint="Enter Password" android:inputType="textPassword" />

 <Button android:id="@+id/btnLogin" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:text="Login" />

 <TextView android:id="@+id/tvResult" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:textSize="16sp" />

</LinearLayout>

Java (MainActivity.java):

-------------------------

package com.example.loginform;

import android.os.Bundle;

import android.widget.*;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

 EditText etUser, etPass;

 Button btnLogin;

 TextView tvResult;

 @Override

 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 etUser = findViewById(R.id.etUser);

 etPass = findViewById(R.id.etPass);

 btnLogin = findViewById(R.id.btnLogin);

 tvResult = findViewById(R.id.tvResult);

 btnLogin.setOnClickListener(v -> {

 String user = etUser.getText().toString();

 String pass = etPass.getText().toString();

 tvResult.setText("Username: " + user + "\nPassword: " + pass);

 });

 }

}
