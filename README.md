Install cleanflight, and add usb driver if needed:

[http://blog.sam-thompson.info/cleanflight-on-mac-osx/](http://blog.sam-thompson.info/cleanflight-on-mac-osx/)

1\) install engines and escs

2\) plug usb and goto cleanflight "motors"

3\) switch motors to full speed

4\) plug battery to escs and wait for esc to beep

5\) go back to 0 level on motors

ESC calibration:

[https://www.reddit.com/r/Multicopter/comments/3vlkg9/please\_help\_one\_motor\_needs\_more\_power\_to\_spin\_up/](https://www.reddit.com/r/Multicopter/comments/3vlkg9/please_help_one_motor_needs_more_power_to_spin_up/)

!! Attention when connecting motors to cable properly the CW \(clockwise motors\) and CCW. The cables needs to be inverted.

[https://www.dronetrest.com/t/esc-to-motor-connection-guide-how-to-reverse-your-motor-direction-the-easy-way/1297](https://www.dronetrest.com/t/esc-to-motor-connection-guide-how-to-reverse-your-motor-direction-the-easy-way/1297)

6\) turnigy remote controller binding

[https://www.youtube.com/watch?v=9-Z0rTVEkHI](https://www.youtube.com/watch?v=9-Z0rTVEkHI)

7\) RX ppm allocation [https://www.youtube.com/watch?v=yN00UdPQdRc&t=72s&pbjreload=10](https://www.youtube.com/watch?v=yN00UdPQdRc&t=72s&pbjreload=10)

7\) uart allocation for controller

[https://www.youtube.com/watch?v=jkl5BU5Heq0](https://www.youtube.com/watch?v=jkl5BU5Heq0)

8\) set up ppm on telecommande,

system setup

RX setup -&gt; select ppm mode on

be sure that the remot receiver is connected on port 1  \(PPM enabled\)

Attention une telecommande peut supporter le PPM \(multiples ports en un seul\), mais pas forcément les recepteurs, par exemple le tgy-ia6 ne fonctionne qu'en PWM

9\) connecting receiver with Naze32:

PPM is off, on the TX? Channel 1 has GND, PWR, and SIG connections between board and RX \(correct orientation\) all others have SIG? Red light on RX is solid?

[http://intofpv.com/t-naze32-rev6-with-flysky-fs-ia6-reciever-problems](http://intofpv.com/t-naze32-rev6-with-flysky-fs-ia6-reciever-problems)

10\) attribuer les actions "gaz..." à la telecommande:

A = aileron =&gt; Roll \(haut bas manette de droite\) x

E = elevator = altitude = pitch \(gauche droite manette de droite\)

T = throttle =&gt; throttle gaz  \(Manette gauche - haut bas\) x

R = Rudder =&gt; Yaw \(man gauche - gauche droite\) x

[https://www.youtube.com/watch?v=v\_0lf1u3F3A](https://www.youtube.com/watch?v=v_0lf1u3F3A)

Pour débugger la transmission et voir sur quel channel est affecté quel bouton, aller dans la telecommande sur le menu setup, puis sur display \(on voit quel canal est affecté par le changement de position d'un bouton\)

[https://www.youtube.com/watch?v=cGYFRCEQ2Ps&t=521s](https://www.youtube.com/watch?v=cGYFRCEQ2Ps&t=521s)

10\) Les modes, startup + types de vols

interface de cleanflight qui permet d'activer des modes sur les boutons de la télécommande:

[https://blog.dronetrest.com/setting-up-flight-modes-in-cleanflight-betaflight/](https://blog.dronetrest.com/setting-up-flight-modes-in-cleanflight-betaflight/)

11\) activate barometer and compass

Barometer is not activated by default but can be done by clicking on a button on tab "configuration" \(en bas de la page\)

==&gt; NAZE32 is an old board and they deactivated compass, but can be reactivated with some tuning on the config files:

[https://github.com/betaflight/betaflight/issues/2165](https://github.com/betaflight/betaflight/issues/2165)

11\) PID tuning:

[https://www.wearefpv.fr/betaflight-3-2-reglages-pid-20170918/](https://www.wearefpv.fr/betaflight-3-2-reglages-pid-20170918/)

[https://open-txu.org/home/special-interests/multirotor/cleanflight-pid-tuning/](https://open-txu.org/home/special-interests/multirotor/cleanflight-pid-tuning/)

12\) to compile cleanflight you need

for mac: [https://github.com/cleanflight/cleanflight/blob/master/docs/development/Building in Mac OS X.md](https://github.com/cleanflight/cleanflight/blob/master/docs/development/Building in Mac OS X.md)

gnu make \(test make\)

gcc for arm

[https://launchpad.net/gcc-arm-embedded/+download](https://launchpad.net/gcc-arm-embedded/+download)

Note sur les differents softs:

Cleanflight a été forké par deux versions:

Betaflight pour le racing

iNav pour la navigation avec waypoints

Note: OSD

On Screen Display:

un petit appareil qui se branche entre la caméra et le tx pour adjoindre a l'écran des informations contextuelles.

AP: auto pilot, généralement connecté à un GPS et un OSD



--&gt; how to fligh your drone:

https://uavcoach.com/how-to-fly-a-quadcopter-guide/\#Controls

Pitch: manette de droite, avant arrière \(penche le drone en avant ou en arrière\)

Roll: manette de droite, gauche ou droite: penche le drone vers la droite ou vers la gauche \(pour tourner\)

Throttle: gaz, accélère les hélices \(le drone accélère dans la direction ou il est penché\)

Yaw: fait tourner le drone sur lui même \(sert plus pour les figures ou les photos, pas pour la direction\)



