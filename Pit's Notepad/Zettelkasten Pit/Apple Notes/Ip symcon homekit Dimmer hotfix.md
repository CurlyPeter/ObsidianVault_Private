https://community.symcon.de/t/dimmer-in-homekit-schaltet-erst-100-und-anschliessend-auf-den-eingestellten-dimmwert/51687/10

sudo nano /var/lib/symcon/modules/.store/de.paresy.homekit/HomeKitBridge/accessories/lightbulbDimmer.php


habe kurz ins HomeKit Bridge Modul reingeschaut und bei

<p style="text-align:center;margin:0">
</p>
modules\HomeKit\HomeKitBridge\accessories\lightbulbDimmer.php
die Anweisung

<p style="text-align:center;margin:0">
</p>
self::dimDevice(**$this**->data['VariableID'], 100); 
auf Zeile 32 auskommentiert
Sieht bei mir ab Zeile 23 jetzt so aus:

<p style="text-align:center;margin:0">
</p>

    **public** **function** **writeCharacteristicOn**($value)
    {
        *//Only switch the device on, if it isn't on.*
        *//This should fix the problem that Apple sends on before dimming*
        **if** ($value && **$this**->readCharacteristicOn()) {
            **return**;
        }

        *//try to avoid lighflash when dimming a lamp from off state, i.e. only allow direct off but not direct on*
        **if** ($value) {            
        *//    self::dimDevice($this->data['VariableID'], 100);*
        } **else** {
            self::dimDevice(**$this**->data['VariableID'], 0);
        }
    }
**Damit habe ich das gewünschte Ergebnis, d.h kein hochdimmen auf 100% vor dem Einstellen des eigentlichen Dimm-Werts.** [**@paresy**](https://community.symcon.de/u/paresy): Schaut doch mal, ob das ggfs. als Lösung in Frage kommt und als Änderung ins GIT Repository einfliessen könnte?
Gruss dolocyl