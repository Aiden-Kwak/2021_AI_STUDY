jupyter notebook에서도 octave kernel 설치를 통해 octave 구동이 가능하다<br>\
plot을 시도했을때 에러가 발생하였다.<br>
Inline plot failed, consider trying another graphics toolkit error: print: figure must be visible or qt toolkit must be used with __gl_window__ property 'on' or QT_OFFSCREEN feature available<br>

우선은 graphics_toolkit ("gnuplot"); 을 이용해 해결하였다.<br>
<br>
주피터에서 하면 엄청 느리다. 제대로 만들땐 octave-cli 에서하자.
