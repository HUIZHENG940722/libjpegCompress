# libjpegCompress
Android libjpegCompress supported armeabi armeabi-v7a arm64-v8a,x86,x84_64
##1.在项目build.gradle添加

   <pre> <code>
allprojects {
		    repositories {
			    maven { url 'https://jitpack.io' }
		    }
	    }
	</code></pre>
	
  ##2.在App module添加
  
  <pre><code>
  dependencies {
	        compile 'com.github.Medivh2011:libjpegCompress:1.1'
	}
	</code></pre>
	
  ##3.Use
  <pre><code>
  ImageCompress
  .with(getApplicationContext())
  .load(imagePath).ignoreBy(100)
  .setTargetDir(savedir)
  .setOnCompressListener(new ImageCompress.OnCompressListener() 
  {
      @Override
      public void onStart() {
        //todo doStart
      }

      @Override
      public void onSuccess(String filePath) {
        //todo douccess
      }

      @Override
      public void onError(Throwable e) {
        //todo doError
      }
    }).launch();
    </code>
    <pre>
    
  
