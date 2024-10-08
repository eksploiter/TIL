# Kakao Map API Authentication

## Dependencies
Below are the key dependencies used in this project:
```groovy
    implementation("com.kakao.sdk:v2-user:2.12.1") // 카카오 로그인 모듈 (keyHash 값 때문에 설정)
    implementation("com.kakao.maps.open:android:2.6.0") // 카카오 맵 API

    // 안드로이드 클라이언트에서 서버와 연결 => Retrofit 을 사용해 서버와 통신
    // Retrofit
    implementation("com.squareup.retrofit2:retrofit:2.9.0")
    implementation("com.squareup.retrofit2:converter-gson:2.9.0")

    // Gson
    implementation("com.google.code.gson:gson:2.8.8")
    implementation ("com.squareup.okhttp3:okhttp:4.9.1")
```
