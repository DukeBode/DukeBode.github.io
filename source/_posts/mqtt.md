---
title: mqtt
date: 2024-05-02 15:12:44
cover: 
tags: 
mathjax: false
---
[MQTT](https://mqtt.org/) 是一种轻量级的、灵活的物联网消息交换和数据传递协议，致力于为 IoT 开发人员实现灵活性与硬件/网络资源的平衡。

<!-- more -->

## 1. Android(Kotlin)

mosquito.conf
```conf
# Starting in local only mode.
# https://mosquitto.org/blog/2020/12/version-2-0-0-released/
listener 1883
allow_anonymous true
```

build.gradle.kts
```kts
dependencies {
implementation("org.eclipse.paho:org.eclipse.paho.client.mqttv3:1.2.5")
    //implementation("org.eclipse.paho:org.eclipse.paho.android.service:1.1.1")
    implementation("io.github.muxiaolin:org.eclipse.paho.android.service:1.1.4")
}
```

AndroidManifest.xml
```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.WAKE_LOCK" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application>
   <service android:name="org.eclipse.paho.android.service.MqttService" />
</application>
```


[mosquitto-MQTT broker](https://mosquitto.org/)
[mosquitto 的安装、配置、使用教程](https://www.cnblogs.com/qumogu/p/16007609.html)
[Starting in local only mode](https://www.cnblogs.com/simadi/p/15666493.html)
[MQTT Client](https://eclipse.dev/paho/index.php?page=downloads.php)
[高Android版本中MqttAndroidClient库无法使用问题:MqttAndroidClient未对AndroidX适配导致](https://blog.csdn.net/kankanlj/article/details/128385271)
[Android 使用 Kotlin 连接 MQTT](https://www.emqx.com/zh/blog/android-connects-mqtt-using-kotlin)
[Paho-MQTT Android接入示例](https://help.aliyun.com/zh/iot/use-cases/use-the-paho-mqtt-android-client?spm=a2c4g.11186623.0.0#section-k7a-kae-iyx)
