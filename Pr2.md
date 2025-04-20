#pr2
MainActivity.java

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.EditText;

import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

private EditText emailEditText, passwordEditText;

private Button registerButton, loginButton;

@Override

protected void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);

setContentView(R.layout.activity_main);

emailEditText = findViewById(R.id.email_edit_text);

passwordEditText = findViewById(R.id.password_edit_text);

registerButton = findViewById(R.id.register_button);

loginButton = findViewById(R.id.login_button);

registerButton.setOnClickListener(v -> {

String email = emailEditText.getText().toString();

String password = passwordEditText.getText().toString();

// Register student logic here

Toast.makeText(this, "Student registered successfully!",

Toast.LENGTH_SHORT).show();

});

loginButton.setOnClickListener(v -> {

String email = emailEditText.getText().toString();

String password = passwordEditText.getText().toString();

// Login student logic here

Toast.makeText(this, "Student logged in successfully!", Toast.LENGTH_SHORT).show();

});

}
}

activity_main.xml

<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

android:layout_width="match_parent"

android:layout_height="match_parent"

android:orientation="vertical">

<EditText

android:id="@+id/email_edit_text"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:hint="Email" />

<EditText

android:id="@+id/password_edit_text"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:hint="Password"

android:inputType="textPassword" />

<Button

android:id="@+id/register_button"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:text="Register" />

<Button

android:id="@+id/login_button"

android:layout_width="match_parent"

android:layout_height="wrap_content"

android:text="Login" />

</LinearLayout>
