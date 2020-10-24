---
layout: itv
title: Interdimentional TV Cable
permalink: /itv
---
<div>
    Interdimentional TV Cable
    <Button>Select</Button>
    <div>
        <!-- 1. The <iframe> (and video player) will replace this <div> tag. -->
    <div id="player"></div>
    <!-- <iframe id="ytplayer" type="text/html" width="720" height="405"
src="https://www.youtube.com/embed/?autoplay=1&enablejsapi=1&list=PLoibju-lZs8u6LOudKJ0-mu_P7Bw6cDZQ&listType=playlist"
frameborder="0" allowfullscreen> -->
    <script>
        // 2. This code loads the IFrame Player API code asynchronously.
        // var tag = document.createElement('script');
        // tag.src = "https://www.youtube.com/iframe_api";
        // var firstScriptTag = document.getElementsByTagName('script')[0];
        // firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);
        // // 3. This function creates an <iframe> (and YouTube player)
        // //    after the API code downloads.
        var player;
        function onYouTubeIframeAPIReady() {
            // player = new YT.Player('player', {
            // height: '390',
            // width: '640',
            // // videoId: 'M7lc1UVf-VE',
            // // playlist: ['M7lc1UVf-VE','Gpsn2P5UY_A'],
            // listType:'playlist',
            // list:'PL4o29bINVT4EG_y-k5jGoOu3-Am8Nvi10',
            // events: {
            //     'onReady': onPlayerReady,
            //     'onStateChange': onPlayerStateChange
            // }
            // });
            // PL4o29bINVT4EG_y-k5jGoOu3-Am8Nvi10
            // player.cueVideoById({videoId:'Gpsn2P5UY_A'});
        }
        // 4. The API will call this function when the video player is ready.
        function onPlayerReady(event) {
            event.target.playVideo();
        }
        // 5. The API calls this function when the player's state changes.
        //    The function indicates that when playing a video (state=1),
        //    the player should play for six seconds and then stop.
        var done = false;
        function onPlayerStateChange(event) {
            if (event.data == YT.PlayerState.PLAYING && !done) {
            setTimeout(stopVideo, 6000);
            done = true;
            }
        }
        function stopVideo() {
            player.stopVideo();
        }
        </script>
    </div>
    <div>
</div>