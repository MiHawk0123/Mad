#pr 5 (Accept Username and Password)
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

 android:layout_height="wrap_content" android:hint="Username" />

 <EditText android:id="@+id/etPass" android:layout_width="match_parent"
android:layout_height="wrap_content" android:hint="Password" android:inputType="textPassword" />

 <Button android:id="@+id/btnSubmit" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:text="Submit" />

 <TextView android:id="@+id/tvDisplay" android:layout_width="wrap_content"

 android:layout_height="wrap_content" android:textSize="16sp" />

</LinearLayout>

Java (MainActivity.java):

-------------------------

package com.example.acceptuserpass;

import android.os.Bundle;

import android.widget.*;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

 EditText etUser, etPass;

 Button btnSubmit;

 TextView tvDisplay;

 @Override

 protected void onCreate(Bundle savedInstanceState) {

 super.onCreate(savedInstanceState);

 setContentView(R.layout.activity_main);

 etUser = findViewById(R.id.etUser);

 etPass = findViewById(R.id.etPass);

 btnSubmit = findViewById(R.id.btnSubmit);

 tvDisplay = findViewById(R.id.tvDisplay);

 btnSubmit.setOnClickListener(v -> {

 String user = etUser.getText().toString();

 String pass = etPass.getText().toString();

 tvDisplay.setText("Username: " + user + "\nPassword: " + pass);

 });

 }

}
