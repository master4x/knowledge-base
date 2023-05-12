# Ethernet-Frame
*Daten*, die über ein Netzwerk verschickt werden, werden nicht als kontinuierlicher Datenstrom (so wie eine Radiosendung) übertragen. Eine gewisse Anzahl von Daten wird zusammengefasst und als *Datenpaket* verschickt. Die Daten, die über ein Ethernet verschickt werden, werden in einen *Frame*, einen Rahmen, eingepackt. Der Frame wird Bit für Bit, seriell, von links nach rechts, über die Leitung übertragen. Der Frame startet mit einem Synchronisationssignal, der *Preamble*. Die Empfänger stellen sich dadurch auf die Übertragungsrate ein, sodass sie jedes Bit zeitgenau einlesen können. Die Preamble gehört jedoch nicht zu den Daten selbst. Sie dient lediglich der Abstimmung mit dem Empfänger.  

Nach der Synchronisation wird die Adresse des Interfaces übertragen, welches die Daten empfangen soll. Dies ist die Adresse der Netzwerkkarte des Zielrechners. Nach der Zieladresse folgt die Absenderadresse. Im Typ-Feld wird angegeben, von welchem Typ die folgenden Nutzdaten sind. Wird als Nutzdaten beispielsweise ein IP-Paket übertragen, so steht hier die Kennung 0x0800.

| Synchronisation | Zielinterface | Absenderinterface | Typ    | Nutzdaten       | Prüfsumme |
|-----------------|---------------|-------------------|--------|-----------------|-----------|
| 8 Byte          | 6 Byte        | 6 Byte            | 2 Byte | 46 - 1.500 Byte | 4 Byte    |

*Interfaceadressen* und *Type* bilden den Protokollkopf oder Header. Zusammen mit der *Prüfsumme* (auch Frame-Check-Sequence oder FCS genannt) werden 18 Byte als „Protokolloverhead“ (Header: Interfaceadressen und Type, Trailer: Prüfsumme) beansprucht. Die Nutzdaten müssen nun mindestens 46 Byte groß sein, damit die **Mindestgröße von 64 Bytes** zur Gewährleistung der Kollisionserkennung erreicht werden kann. Die maximale Größe beträgt 1500 Byte.
