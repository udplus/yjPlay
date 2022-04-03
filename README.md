# yjPlay

[![Download](https://api.bintray.com/packages/ycjiang/ycjiang/VideoPlayModule/images/download.svg) ](https://bintray.com/ycjiang/ycjiang/VideoPlayModule/_latestVersion)


  ### gif 비트 카드를 표시하면 프레임 수가 낮 으면 실제가 매우 부드럽습니다.
  #### [다운로드 미리보기 APK.](https://raw.githubusercontent.com/yangchaojiang/yjPlay/master/app-release.apk)

 ![](https://github.com/yangchaojiang/ResProject/blob/master/gif/test.gif)  ![](https://github.com/yangchaojiang/ResProject/blob/master/gif/test2.gif)
 
 ![](https://github.com/yangchaojiang/ResProject/blob/master/gif/test3.gif)
 ![](https://github.com/yangchaojiang/ResProject/blob/master/gif/test4.gif)

  ![](https://github.com/yangchaojiang/ResProject/blob/master/gif/testtv.gif)
 ### 외계인 기반 맞춤 플레이어 JPlayer지원 기능：
   *  ExoUserPlayer 기본 재생 (기본 닫힌 제스처) 밝기, 볼륨, 빨리 감기, 동등한 제스처, 지원 사용자 정의 레이아웃)
   *  자동으로 적응 TV 적응.
   *  수평 화면과 수직 화면의 전체 화면을 지원하십시오.
   *  오디오 제어 레이아웃에 적용됩니다.
   *  광고 비디오 미리보기를 지원합니다(달성하기 쉽고 완벽하게 처리합니다.<font color="red">사용자 정의</font>)。
   *  여러 해상도 비디오 스위치를 지원합니다 (사용자 정의 레이아웃 스타일이 지원됨).
   *  [캐시 다운로드 암호화 비디오 기능 (벤치 캐시가 쉬운)](README_EN_VIDEO.md)<font color="red">AndroidVideoCACCHE를 사용하지 않습니다</font>。
   *  지원 목록 컬렉션 동영상 재생 (<font color="red">세부 사항에 대한 목록은 완벽한 과도하게 재생됩니다</font>）
   *  지원 네트워크 유형 팁 재생 여부(사용자 정의)。
   *  비디오로드 레이아웃, 오류 레이아웃, 재생 레이아웃, 프롬프트 레이아웃 사용자 정의,보다 유연한 레이아웃 스타일의 유연한 구현을 지원합니다.
   * 비디오 가속도 지원 천천히 재생 (지원되는 사용자 정의 레이아웃 스타일) 참조 데모 사용자 정의.
   * 다중 비디오 커버 맵을 지원합니다 (두 가지 모드 커버).
   * 사용자 정의 [MediaSource] ()를 지원하는 지원.
   * 간소화 및 정식 버전을 지원하고, 더 부유를 사용하도록 선택하십시오.
   *  [오프라인 다운로드 2 차를 추가하십시오 ExoWholeDownLoadManger,ExoWholeDownloadTracker,ExoDownLoadManger,DownloadService()-->戳我](README_EN_VIDEO.md))
   *  지원 재생 잠금 화면 기능 및 제어 레이아웃 표시 디스플레이 애니메이션 효과.
   * 뒤로 버튼 및 전체 화면 버튼 아이콘 사용자 정의 지원.
   * 사용자 정의 비디오 커버 레이아웃을 지원합니다. (비디오 표지 다이어그램 레이아웃 스타일이 완벽합니다).
   * 비디오 실시간 진행 (헤드 라인의 맨 아래)을 지원합니다.
   * 스트리밍 API 모드 호출을 지원합니다.
   *  여러 파일 유형을 지원합니다，MP4，M4A，WebM，Matroska,Ogg,WAV，MP3，MPEG-TS，MPEG-PS，FLV，ADTS (AAC)，Flac，M3U8,mkv 等。
   *  사용자 정의 복수 지원 http,Rtmp,Https,Cronet 等协议。
 <!--more-->

 ### [업데이트 로그2.3.51→》나를 찌르다](RELEASENOTES.md)


 ### 一.참조 클래스 라이브러리
  ````
   repositories {
          jcenter()
          mavenCentral();
      }

  dependencies {
     //풀 버전
      compile 'com.ycjiang:VideoPlayModule:2.3.61'
     //精简版（没有smoothstreaming,dash,hls,只有常规点播功能）
      compile 'com.ycjiang:VideoPlayModule-Lite:2.3.61'

  }
  ````
  >>> 팁 : 정상을 인용 할 수없는 경우 repositories{ }코드를 추가하십시오
  >>> mavenCentral(url: "https://dl.bintray.com/ycjiang/ycjiang")

 ### 二.제어 속성
   >>>> 기본적으로 다음과 같이 사용됩니다
   ````
         <chuangyuan.ycj.videolibrary.widget.VideoPlayerView
                 android:id="@+id/exo_play_context_id"
                 android:layout_width="match_parent"
                 android:layout_height="match_parent"
                 android:background="@android:color/transparent"
                 />
 ````
 >>  #### 1.제어 속성
 ````
   <chuangyuan.ycj.videolibrary.widget.VideoPlayerView
         android:id="@+id/exo_play_context_id"
         android:layout_width="match_parent"
         android:layout_height="match_parent"
         app:controller_layout_id="@layout/simple_exo_playback_control_view"
         app:player_layout_id="@layout/simple_exo_view"
         app:player_replay_layout_id="@layout/custom_play_replay"
         app:player_error_layout_id="@layout/custom_play_error"
         app:player_hint_layout_id="@layout/custom_play_btn_hint"
         app:player_load_layout_id="@layout/custom_exo_play_load"
         app:player_gesture_audio_layout_id="@layout/custom_gesture_audio"
         app:player_gesture_bright_layout_id="@layout/custom_gesture_brightness"
         app:player_gesture_progress_layout_id="@layout/custom_gesture_pro"
         app:player_preview_layout_id="@layout/exo_default_preview_layout"
         app:resize_mode="fit"
         app:show_timeout="3000"
         app:surface_type="texture_view"
         app:fastforward_increment="0"
         app:rewind_increment="0"
         app:user_watermark="@mipmap/watermark_big"
         app:player_list="true"
         app:use_controller="true"
         app:player_fullscreen_image_selector="@drawable/custom_full_selector"
         app:player_back_image="@drawable/ic_back_custom"
          />
   ````
   
 >> #### 2.속성 설명 사용자 정의보기 사용 가능한 속성 :
  
  | name                              | type      | info                                                                        |
  |-----------------------------------|-----------|---------------------------------------------------------------------------- |
  | surface_type                      | enum      | 비디오 렌더링 유형 texture_view 和surface_view 열거 된 유형 默认surface_view          |  
  | resize_mode                       | enum      | 비디오 줌 렌더링 디스플레이 모드는 5입니다                                                 |
  |                                   | reference | 1.fit          일반 모드                                                     | 
  |                                   | reference | 2.fixed_16_9  비디오 비율 유지 관리 16:9                                        | 
  |                                   | reference | 3.fixed_4_3   비디오 비율 유지 4:3                                           |         
  |                                   | reference | 4.fill           전체 화면 모드, 스트레치 비디오 와이드                                     |        
  |                                   | reference | 4.match          매트릭스 모드                                                 |      0
  | player_layout_id                  | reference | (플레이어 레이아웃):현재 기본 레이아웃  simple_exo_view.xml                              |
  | controller_layout_id              | reference | 컨트롤러 레이아웃  기본적으로 네 개의 레이아웃이 있습니다                                                  |
  |                                   | reference | 1.simple_exo_playback_control_view.xml  비디오 커버 제어 레이아웃,(기본)       | 
  |                                   | reference | 2.simple_exo_playback_list_view.xml.xml 목록에서 사용 제어 레이아웃을 재생하십시오              | 
  |                                   | reference | 3.simple_exo_playback_top_view.xml.xml  视频封面控制布局上面                |
  |                                   | reference | 4.exo_playback_control_view.xml         exo 提供默认风格                    | 
  | player_replay_layout_id           | reference | 设置 自定义重播布局文件                                                     |
  | player_error_layout_id            | reference | 设置 自定义错误布局文件                                                     |
  | player_hint_layout_id             | reference | 设置 自定义非wifi提示布局文件                                               |
  | player_load_layout_id             | reference | 设置 自定义视频加载布局文件                                                 |
  | player_gesture_audio_layout_id    | reference | 设置 自定义手势音频调节布局                                                 |
  | player_gesture_bright_layout_id   | reference | 设置 自定义手势亮度调节布局                                                 |
  | player_gesture_progress_layout_id | reference | 设置 自定义手势进度调节布局                                                 |
  | player_preview_layout_id          | reference | 设置 自定义封面图布局(默认 exo_default_preview_layout.xml)                  |
  | player_list                       | boolean   | 设置 是否指定列表播放    默认 false  true 列表播放                          |
  | player_fullscreen_image_selector  | reference | 设置 自定义全屏按钮selector                                                 |
  | player_back_image                 | reference | 设置 自定义返回按钮图标                                                     |
  | default_artwork                   | reference | 设置 封面占位图                                                             |
  | show_timeout                      | integer   | 设置 控制布局隐藏时间  默认值为3秒                                          |
  | fastforward_increment             | integer   | 设置 按钮设置快进增量,以毫秒为单位（exo控制布局使用）                       |
  | rewind_increment                  | integer   | 设置 按钮设置快退增量,以毫秒为单位（exo控制布局使用）                       |
  | user_watermark                    | reference | 设置 水印图片 默认在右上角                                                  |

   * **알아 채다:**
     >>    1.목록 재생은 선택할 수 있습니다 texture_view 선택할 수 없습니다 Surface_view, 세부 정보 페이지 재생 권장 사항 surface_view
     >>
     >>    2.사용자 지정 전체 화면 버튼 selector
           
           <selector xmlns:android="http://schemas.android.com/apk/res/android">
                <item android:drawable="@drawable/ic_custom_full" android:state_checked="true" />
                <item android:drawable="@drawable/ic_custom_full_in" android:state_checked="false" />
           </selector>
    
     >>       
     >>        
     >>   3.사용자 정의 커버 다이어그램 레이아웃,또한 또한 포함되어 있습니다
  >> #### 3.빠른 사용자 정의 비디오 진행률 색상
   >> [如何自定义视频进度控件--->戳我](https://github.com/yangchaojiang/yjPlay/blob/dev/READMELAYUOT.md#%E4%BA%94%E8%A7%86%E9%A2%91%E6%92%AD%E6%94%BE%E8%BF%9B%E5%BA%A6%E6%8E%A7%E4%BB%B6%E8%87%AA%E5%AE%9A%E4%B9%89)
  >> 在app的module的values 文件下-> colors.xml 文件里
   ```
     <!--비디오로드 캐시 진행률 만족도.따라서 표지 차트 레이아웃을 사용자 정의하면 덮개 맵 컨트롤을 사용하여 제어 레이아웃을 사용하지 마십시오.
                   颜色-->
     <color name="timeBar_buffered_color">@color/light_green</color>
     <!--已经播放过视频的颜色-->
     <color name="timeBar_played_color">#c63020</color>
     <!--没有加载过进度的颜色-->
     <color name="timeBar_unplayed_color">@color/live_yellow</color>
     <!--视频进度圆点的颜色-->
     <color name="timeBar_scrubber_color">@color/colorAccent</color>
     
   ```
 >> #### 4.네트워크 수정 대화 상자 프롬프트 텍스트 콘텐츠
      app.strings.xml
      <string name="exo_play_reminder">您当前网络不是wifi，是否继续观看视频</string>
      <string name="exo_play_wifi_hint_no">提示</string>
 >> #### 5.전체 화면 모드를 켭니다.
     ```
     VideoPlayerView.setVerticalFullScreen(true)
     ```
     或者
     ````
       exoPlayerManager = new VideoPlayerManager.Builder(VideoPlayerManager.TYPE_PLAY_GESTURE, videoPlayerView)
                     .setVerticalFullScreen(true)
     ````

 >> #### 6.함수 목록의 선언문 AndroidManifest.xml
    在activity节点 加上“android:configChanges="orientation|keyboardHidden|screenSize"”
     如下实例：
            <activity android:name="chuangyuan.ycj.yjplay.MainListActivity"
             android:configChanges="orientation|keyboardHidden|screenSize"
             android:screenOrientation="portrait">


      

 ### 3.JAVA 암호

 > #### 1 재생 제어 클래스
    1.ExoUserPlayer

 > #### 2 VideoPlayerView 제어 사용 가능한 방법
  | name                                           | type      | info                                                                        |
|------------------------------------------------|-----------|---------------------------------------------------------------------------- |
| setTitle("제목")                               | void      | 비디오 제목을 설정하십시오                                                               | | |
| setExoPlayWatermarkImg(R.mipmap.watermark_big) | void      | 워터 마크 추가 사진을 설정하십시오                                                               | | |
| setPreviewImage(Bitmap）                       | void      | 덮개 맵을 설정하십시오                                                             | | |
| setPreviewImage(R.res.image)                   | void      | 덮개 맵을 설정하십시오                                                                | | |
| setPreviewImage(R.res.image)                   | void      | 덮개 맵을 설정하십시오                                                                | | |
| getPreviewImage()                              | ImageView | 덮개 맵 제어를 설정하십시오                                                               | | |
| setPreviewImage(R.res.image)                   | void      | 덮개 맵을 설정하십시오                                                                | | |
| setVerticalFullScreen(true)                    | void      | 수직 화면 전체 화면을 엽니 다                                                           |
  >>더 많은 방법 참조 데모 사용법.
  
 > #### 3 재생 코드 
                  //instantiate.
         ExoUserPlayer exoPlayerManager = new VideoPlayerManager.Builder(VideoPlayerManager.TYPE_PLAY_MANUAL, videoPlayerView)
                          .setDataSource(new DataSource(this))
                          //加载rtmp 协议视频
                          .setPlayUri("rtmp://live.hkstv.hk.lxdns.com/live/hks")
                          //加载m3u8
                          .setPlayUri("http://dlhls.cdn.zhanqi.tv/zqlive/35180_KUDhx.m3u8")
                          //加载ts.文件
                          .setPlayUri("http://185.73.239.15:25461/live/1/1/924.ts")
                          //播放本地视频
                          .setPlayUri("/storage/emulated/0/DCIM/Camera/VID_20170717_011150.mp4")
                          //播放列表视频
                          .setPlayUri(listss);
                          //设置开始播放进度
                          .setPosition(1000)
                          //示例本地路径 或者 /storage/emulated/0/DCIM/Camera/VID_20180215_131926.mp4
                          .setPlayUri(Environment.getExternalStorageDirectory().getAbsolutePath()+"/VID_20170925_154925.mp4")
                          //开启线路设置
                          .setShowVideoSwitch(true)
                          .setPlaySwitchUri(0,test,name)
                          .setPlaySwitchUri(0, 0, getString(R.string.uri_test_11), Arrays.asList(test), Arrays.asList(name))
                          //设置播放视频倍数  快进播放和慢放播放
                          .setPlaybackParameters(0.5f, 0.5f)
                          //是否屏蔽进度控件拖拽快进视频（例如广告视频，（不允许用户））
                          .setSeekBarSeek(false)
                          //设置视循环播放
                          .setLooping(10)
                          //视频进度回调
                           .addOnWindowListener(new VideoWindowListener() {
                                             @Override
                                             public void onCurrentIndex(int currentIndex, int windowCount) {
                                                 Toast.makeText(getApplication(), currentIndex + "windowCount:" + windowCount,                                                    Toast.LENGTH_SHORT).show();
                                             }
                                         })
                          .addOnWindowListener(new VideoWindowListener() {
                              @Override
                              public void onCurrentIndex(int currentIndex, int windowCount) {
                                  Toast.makeText(getApplication(), currentIndex + "windowCount:" + windowCount, Toast.LENGTH_SHORT)                                             .show();
                              }
                          })
                          .addVideoInfoListener(new VideoInfoListener() {
                              ·····
                          })
                          //创建
                           .create()
                             //播放视频
                          .startPlayer();

   1.인스턴스화 재생 제어 클래스
          //播放控制器创建
           ExoUserPlayer exoPlayerManager = new VideoPlayerManager.Builder(VideoPlayerManager.TYPE_PLAY_USER, videoPlayerView).create();

   2.데이터 소스를 사용자 정의하고 나중에 데이터 소스 클래스를 사용자 정의하는 방법을 설명합니다.

         ExoUserPlayer exoPlayerManager = new VideoPlayerManager.Builder(VideoPlayerManager.TYPE_PLAY_MANUAL, videoPlayerView)
                                                        .setDataSource(new DataSource(this))
                                                        .create();
         ExoUserPlayer exoPlayerManager =  new VideoPlayerManager.Builder(VideoPlayerManager.TYPE_PLAY_MANUAL, videoPlayerView)
                                                          .setDataSource(mediaSourceBuilder)
                                                          .create();
         定义多媒体
         MediaSourceBuilder   mediaSourceBuilder=new MediaSourceBuilder(this,new DataSource(getApplication()));
        集成smoothstreaming,dash,hls
         WholeMediaSource   mediaSourceBuilder=new MediaSourceBuilder(this,new DataSource(getApplication()));  
         ManualPlayer   exoPlayerManager =new VideoPlayerManager.Builder(VideoPlayerManager.TYPE_PLAY_MANUAL, videoPlayerView)
                                                            .setDataSource(mediaSourceBuilder)
                                                            .create();

 > #### 4 VideoPlayerManager.Builder 재생 관리 클래스 사용 가능한 방법
  | name                                 | type | info                                                                        |
  |--------------------------------------|------|---------------------------------------------------------------------------- |
  | setPosition(1000)                    | void |  设置开始播放进度                                                               |  
  | setPosition(windowIndex,1000)        | void |  设置设置当前窗口位置,开始播放进度                                                               |  
  | setPlayUri("http:...m3u8");          | void |  设置视频路径                                                             |  
  | setPlayUri(Uri.parse("uri"))         | void |  设置开始播放进度                                                               |  
  | setShowVideoSwitch(true)             | void |  设置开启多线路设置，默认关闭                                                             |  
  | setLoadModel(LoadModelType.PERCENR)  | void |  设置视频加载提示显示模式（默认LoadModelType.SPEED (网速模式)）                                                            |  
  | setPlaybackParameters(2f,1f)         | void |  设置播放视频倍数  快放和慢放播放 小于1 慢放 大于1 快放  
  | startPlayer()                        | void |  开始播放视频                                                               |  
   
   >>更多方法参考demo用法。
   
 >**알아 채다**
  >> 1.exoPlayerManager.setPlayUri(Environment.getExternalStorageDirectory().getAbsolutePath()+"/test.h264"); 로컬 비디오
  >> 2.멀티 라인 플레이를 설정하십시오
 ````     
            다중 줄 설정을 켜고 기본값을 닫습니다.
            exoPlayerManager.setShowVideoSwitch(true);
            支持List列表
            String [] test={"http://120.25.246.21/vrMobile/travelVideo/zhejiang_xuanchuanpian.mp4",
            "http://120.25.246.21/vrMobile/travelVideo/zhejiang_xuanchuanpian.mp4",
            http://120.25.246.21/vrMobile/travelVideo/zhejiang_xuanchuanpian.mp4"};
            String[] name={"超清","高清","标清"};
            exoPlayerManager.setPlaySwitchUri(0,test,name);
            多分辨路和广告视频设置
            exoPlayerManager.setPlaySwitchUri(0, 0, getString(R.string.uri_test_11), Arrays.asList(test), Arrays.asList(name));
        
 ````
  >>  3.광고 비디오 미리보기(쉬운 구현)
        
          /**需要添加参数就行**/
            第一个参数代表是广告视频位置索引
            exoPlayerManager.setPlayUri(0, "http://mp4.vjshi.com/2013-07-25/2013072519392517096.mp4", "http://mp4.vjshi.com/2013-11-11/1384169050648_274.mp4");       
             如果自己在播放视频时特出处理。实现该接口回调
            视频切换回调处理，进行布局处理，控制布局显示
            exoPlayerManager.setOnWindowListener(new VideoWindowListener() {
            @Override
            public void onCurrentIndex(int currentIndex, int windowCount) {
                         if (currentIndex == 0) {
                             //屏蔽控制布局
                             exoPlayerManager.hideControllerView();
                             //如果屏蔽控制布局 但是需要显示全屏按钮。手动显示，播放正常时自动还原。无需里出
                             videoPlayerView.getExoFullscreen().setVisibility(View.VISIBLE);
                         } else {
                             //恢复控制布局
                             exoPlayerManager.showControllerView();
                         }
                     }
             });
           //跳过广告视频操作
           exoPlayerManager.next();
  >> 4.설정 비즈니스를 처리하려면 재생 버튼을 클릭하십시오
    
      exoPlayerManager.setOnPlayClickListener(new View.OnClickListener() {
                              @Override
                              public void onClick(View v) {
                                  Toast.makeText(MainCustomActivity.this,"定义点击播放事件",Toast.LENGTH_LONG).show();
                                   //处理业务操作 完成后 
                                  exoPlayerManager.startPlayer();//开始播放
                    }
         });
    
  >> 5.모니터 콜백 설정 VideoInfoListener
   
         exoPlayerManager.addVideoInfoListener(new VideoInfoListener() {
                       @Override
                       public void onPlayStart() {
                             //开始播放
                       }

                       @Override
                       public void onLoadingChanged() {
                                 //加载变化
                       }

                       @Override
                       public void onPlayerError(ExoPlaybackException e) {
                                 //加载错误
                      }

                       @Override
                       public void onPlayEnd() {
                              //播放结束
                       }
                       @Override
                       public void onRepeatModeChanged(int repeatMode) {
                           //模式变化
                       }
                   });
   
   >> 6.덮어 쓰기 Activity 그리고 Fragment 사이클 방법

                Override
                public void onResume() {
                    super.onResume();
                    exoPlayerManager.onResume();
                }

                @Override
                public void onPause() {
                    super.onPause();
                    exoPlayerManager.onPause();
                }


                @Override
                protected void onDestroy() {
                    exoPlayerManager.onDestroy();
                    super.onDestroy();
                }

                @Override
                public void onConfigurationChanged(Configuration newConfig) {
                    exoPlayerManager.onConfigurationChanged(newConfig);//横竖屏切换
                    super.onConfigurationChanged(newConfig);
                }
                
                @Override
                public void onBackPressed() {
                //使用播放返回键监听
                 if(exoPlayerManager.onBackPressed()){
                     finish();
                 }
                }


### 三.[목록 지침 목록-->나를 찌르다](RELEASEVIDEO_LIST.md)

### 四.데이터 소스 공장
 ####  1.기본 데이터 원본
          은닉처 : CacheDataSourceFactory
          http : DefaultDataSourceFactory,DefaultHttpDataSourceFactory
          Priority : PriorityDataSourceFactory
 #### 2 ExoPlayer 사용자 정의 데이터 소스 참조 (귀하의 필요에 따라 선택됨)
      compile 'com.google.android.exoplayer:extension-okhttp:2.9.5'
      compile 'com.google.android.exoplayer:extension-rtmp:2.9.5'
      compile 'com.google.android.exoplayer:extension-gvr:2.9.5'
      compile 'com.google.android.exoplayer:extension-cast:2.9.5'
      compile 'com.google.android.exoplayer:extension-mediasession:2.9.5'
      compile 'com.google.android.exoplayer:extension-ima:2.9.5'
      compile 'com.google.android.exoplayer:extension-leanback:2.9.5'

### 五.[사용자 정의 데이터 원본-戳我](RELEASESOURCE.md)
### 六.[사용자 정의 레이아웃-戳我](READMELAYUOT.md)
### 七.[사용자 정의 MediaSource 사용-戳我](RELEASEVIDEO.md) 
### 八.[은닉처,암호화, 비디오 처리 사용-戳我](README_EN_VIDEO.md) 

 ### 혼란스러운 진술
   -dontwarn chuangyuan.ycj.**
   
   -keep class chuangyuan.ycj.** { *;}
 
 
## [License](https://github.com/yangchaojiang/yjPlay/blob/master/LICENSE)
   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.


