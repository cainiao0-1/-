下载Termux
下载地址:https://f-droid.org/packages/com.termux/

注:1.都选Y
      2.文件名自定义

更新源
pkg update

换源
termux-change-repo
选择第一个即可
选择TUNA或BFSU

安装FFmpeg
pkg install ffmpeg

在文件管理软件里创建一个新的文件夹

授予访问文件权限
termux-setup-storage

进入创建的文件夹
cd /storage/emulated/0/文件夹名

开始切片

转格式
ffmpeg -y -i 文件名.mp4 -vcodec copy -acodec copy -vbsf h264_mp4toannexb 文件名.ts

Ts切片
ffmpeg -i 文件名.ts -c copy -map 0 -f segment -segment_list 文件名.m3u8 -segment_time 5 文件名%03d.ts

切片完成

上传

创建Github账号

新建仓库
填个仓库名字就可以了

在Github仓库建立文件夹

新建文件


文件名输入[文件夹/]后任意文件名


上传文件

进入仓库中新建的文件夹
上传文件


全部上传

等待上传成功后确认

上传成功

删除刚刚建立的文件

完成

视频地址
https://cdn.jsdelivr.net/gh/Github账号名/仓库名/文件夹名/文件名.m3u8

添加网页
<div id="dplayer"></div>
<script src="https://cdn.jsdelivr.net/npm/hls.js@0.14.9/dist/hls.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/dplayer@1.26.0/dist/DPlayer.min.js"></script>
<script>
  const dp = new DPlayer({
  container: document.getElementById('dplayer'),
  video: {
      url: '视频地址',
      type: 'hls',
  },
  pluginOptions: {
      hls: {
          // hls config
      },
  },
});
console.log(dp.plugins.hls);
</script>
