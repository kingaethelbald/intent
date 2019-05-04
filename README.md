# intent

主要代码：
```
package com.example.a26081.a5;

import android.content.Intent;
import android.net.Uri;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    private EditText editText;
    private Button button;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    public void onClick(View view){
        Intent intent=new Intent();
        editText=findViewById(R.id.et);
        intent.setAction("android.intent.action.VIEW");
        String url=editText.getText().toString();
        intent.putExtra("address",url);
        startActivity(intent);

    }



}
```
```
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <EditText
        android:id="@+id/et"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="http://www.baidu.com"
        app:layout_constraintLeft_toRightOf="parent"
        app:layout_constraintRight_toLeftOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        />
    <Button
        android:id="@+id/b"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="浏览该网页"
        android:onClick="onClick"
        app:layout_constraintTop_toBottomOf="@id/et"
        app:layout_constraintRight_toLeftOf="parent"
        app:layout_constraintLeft_toRightOf="parent"/>
</android.support.constraint.ConstraintLayout>
```

截图：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190504180002190.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tpbmdhZXRoZWxiYWxk,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190504180019425.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tpbmdhZXRoZWxiYWxk,size_16,color_FFFFFF,t_70)




