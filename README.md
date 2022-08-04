# 我的世界 基岩版 音乐播放器

## 利用button来实现音乐播放
<pre><code class="language-bash"style="">
"button@common.button": {
   "sound_name": "random.click",/音乐名称
   "sound_volume": 1.0//音量大小
  }<span class="token operator"></code></pre>
  
  ## sound_definitions.json
  
  <pre><code class="language-bash"style="">"record.strad"/*音乐名称*/: {
    "sounds": [
      {
        "name": "sounds/music/game/records/strad",//音乐文件路径 注：只能OGG或FSB编码
        "stream": fasle,//是否可以不重叠播放
        "load_on_low_memory": true//使用低负载
      }
    ]
  }<span class="token operator"></code></pre>
  
  ## 暂停的实现
  
  在 sound_definitions.json 内
  <pre><code class="language-bash"style="">"stream": true<span class="token operator"></code></pre>
  相同的音乐不可重叠播放
   
  在 button 内
  
  <pre><code class="language-bash"style="">"sound_volume": 0.000000001//音量大小</code></pre>
  就可以实现关闭音乐了 
  
  注：相同音乐才可暂停
