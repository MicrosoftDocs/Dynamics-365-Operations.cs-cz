---
title: "Přehled maloobchodní periferní zařízení"
description: "Toto téma vysvětluje základní pojmy související s maloobchodní periferní zařízení. Popisuje různé způsoby, že periferní zařízení může být připojeno k místu prodeje (POS) a komponenty jsou odpovědné za správu připojení s POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Přehled maloobchodní periferní zařízení

[!include[banner](includes/banner.md)]


Toto téma vysvětluje základní pojmy související s maloobchodní periferní zařízení. Popisuje různé způsoby, že periferní zařízení může být připojeno k místu prodeje (POS) a komponenty jsou odpovědné za správu připojení s POS.

<a name="concepts"></a>Koncepty
--------

### <a name="pos-registers"></a>Registry POS

Navigace: Klepněte na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**registruje**. Místa prodeje (POS) registr je entita, která se používá k definování vlastností konkrétní instance POS. Tyto vlastnosti zahrnují hardwarový profil nebo instalační program pro maloobchodní periferní zařízení, které budou použity na rejstříku, úložiště, namapovaný na Žurnál a vizuální zážitek pro uživatele, kteří se přihlásí do tohoto rejstříku.

### <a name="devices"></a>Zařízení

Navigace: Klepněte na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**zařízení**. Zařízení je entita, která představuje fyzickou instanci zařízení, která je namapována k pokladně POS. Při vytvoření zařízení je mapována na POS registru. Zařízení sleduje informace o tom, kdy dojde k aktivaci pokladny POS, typu používaného klienta a balíčku aplikace, který byl nasazen na konkrétní zařízení. Zařízení lze mapovat na následující typy aplikací: moderní Retail POS, Cloud program Retail POS, Retail moderní POS – Windows Phone, program Retail POS moderní – Android a Retail POS moderní – iOS.

### <a name="retail-modern-pos"></a>Moderní Retail POS

Moderní POS je program Retail POS pro systém Microsoft Windows. Mohou být nasazeny v operačních systémech Windows 10 (OSs).

### <a name="cloud-pos"></a>Shluk POS

Shluk POS je verze prohlížeče moderní POS program, který je přístupný ve webovém prohlížeči.

### <a name="modern-pos-for-ios"></a>Moderní POS pro iOS

Moderní POS pro iOS je systémem iOS verze programu moderní POS, která může být nasazena na iOS zařízeních.

### <a name="modern-pos-for-android"></a>Moderní POS pro Android

Moderní POS pro Android se systémem Android verzi programu moderní POS, která může být nasazena na Android zařízení.

### <a name="pos-peripherals"></a>Příslušenství POS

POS periferie jsou zařízení, které jsou explicitně podporovány funkce POS. Tato periferní zařízení jsou obvykle rozděleni do konkrétní třídy. Další informace o těchto třídách naleznete v části "Zařízení třídy" tohoto tématu.

### <a name="hardware-station"></a>Hardwarová stanice

Navigace: Klepněte na **maloobchodní a commerce**&gt;**kanály**&gt;**maloobchodní obchody**&gt;**všechny maloobchodní obchody**. Vyberte obchod a potom klikněte na pevnou záložku **Hardwarové stanice**. **Hardware stanice** nastavení je kanál úroveň nastavení, které slouží k definování instance, kde bude nasazen maloobchodní periferní logiku. Toto nastavení na úrovni kanálu se používá k určení vlastnosti hardwaru stanice. Slouží také k seznamu hardwaru stanice, které jsou k dispozici pro moderní POS instance v daném úložišti. Hardwarová stanice je součástí moderní POS program pro systém Windows. Hardwarová stanice lze také implementovat nezávisle jako samostatný program Internetová informační služba (IIS). V tomto případě je přístupný prostřednictvím sítě.

### <a name="hardware-profile"></a>Profil hardwaru

Navigace: Klepněte na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily**. Hardwarový profil je uveden seznam zařízení, která jsou nakonfigurována Pokladna POS nebo hardware stanice. Profil hardwaru lze namapovat přímo do registru POS nebo hardware stanice.

## <a name="devices-classes"></a>Zařízení třídy
Periferní zařízení POS jsou obvykle rozděleny do tříd. Tato část popisuje a poskytuje přehled zařízení, které podporuje moderní POS.

### <a name="printer"></a>Tiskárna

Nabízejí tradiční POS příjmu a celou stránku. Tiskárny jsou podporovány prostřednictvím Object Linking and Embedding Retail POS (OPOS) a Microsoft Windows ovladač rozhraní. Současně lze použít maximálně dvě tiskárny. Tuto funkci podporuje scénáře, kde jsou příjmy cash-and-carry odběratele tisk na tiskárnách potvrzení, že objednávky zákazníků, které bude obsahovat další informace, budou vytištěny na celou stránku tiskárny. Příjem tiskárny můžete připojený přímo k počítači pomocí USB, připojené k síti přes Ethernet nebo připojení přes Bluetooth.

### <a name="scanner"></a>Skener

Až dva čárový kód skenery lze současně. Tato funkce podporuje scénáře skener, který je více mobilní vyžadující ke skenování velkých nebo těžkých položek, zatímco pevné vložené skener se používá pro většinu položek standardní velikosti pro urychlení doby rezervace. Skenery mohou být podporovány prostřednictvím OPOS, Universal Windows Platform (UWP) nebo klávesnice wedge rozhraní. USB nebo technologie Bluetooth umožňuje připojit skener k počítači.

### <a name="msr"></a>MSR

Jeden USB čtečka magnetického proužku (MSR) lze nastavit pomocí ovladače OPOS. Pokud chcete použít samostatný oddíl MSR pro prostředky elektronického přenosu (EFT) platební transakce, musí být spravován konektor platby oddíl MSR. Samostatné MSRs lze použít pro položku věrného zákazníka přihlášení zaměstnance a položku dárkové karty, nezávisle na konektor platby.

### <a name="cash-drawer"></a>Zásuvku

Dvě zásuvky mohou být podporovány na jeden profil hardwaru. Tato funkce umožňuje dvě aktivní směny jedné registrační pokladně je k dispozici ve stejnou dobu. V případě sdílených shift nebo hotovostí, který je používán více mobilních zařízení POS současně je povolen pouze jednu zásuvku na jeden profil hardwaru. Zásuvky můžete připojený přímo k počítači pomocí USB, připojen k síti nebo připojení k tiskárně stvrzenek prostřednictvím rozhraní RJ12. V některých případech mohou být také propojeny zásuvky přes Bluetooth.

### <a name="line-display"></a>Řádkový displej

Zobrazí řádek slouží k zobrazení produktů, zůstatky transakce a další užitečné informace zákazníkovi během transakce. Zobrazení jednoho řádku lze připojit k počítači prostřednictvím USB pomocí ovladače OPOS.

### <a name="signature-capture"></a>Zaznamenání podpisu

Sběr podpisů lze připojit přímo k počítači pomocí USB pomocí ovladače OPOS. Zaznamenání podpisu nakonfigurován, zákazník vyzván k přihlášení na zařízení. Po podpisu je k dispozici, zobrazí se pro pokladníka k přijetí.

### <a name="scale"></a>Měřítko

Měřítka lze připojit k počítači prostřednictvím USP pomocí ovladače OPOS. Pokud produkt, který je označen jako "Weighed" produkt je přidán k transakci, POS načteme stupnice hmotnosti produktu přidá k transakci a používá množství, které podle měřítka.

### <a name="pin-pad"></a>Klávesnice pro kód PIN

Osobní identifikační číslo (PIN) vložky jsou podporovány prostřednictvím OPOS, ale musí být spravovány prostřednictvím konektoru platby.

### <a name="secondary-display"></a>Sekundární monitor

Při konfiguraci sekundární grafické zobrazení Windows číslo 2 se používá k zobrazení základních informací. Účelem sekundární monitor je podporovat rozšíření dodavatele (ISV) nezávislé výrobce softwaru, protože mimo pole sekundární monitor není konfigurovatelné a zobrazuje pouze omezený obsah.

### <a name="payment-device"></a>Platební zařízení

Podpora zařízení platby je implementována prostřednictvím konektoru platby. Zařízení platbu můžete provést jednu nebo mnoho funkcí, které poskytují jiné třídy zařízení. Platební zařízení může například pracovat jako čtečka MSR/karet, zobrazení řádku, podpis digitalizační zařízení a klávesnice pro kód PIN. Podpora pro platební zařízení prováděna nezávisle na podporu samostatné zařízení, která je k dispozici pro další zařízení, která jsou součástí hardwarového profilu.

## <a name="supported-interfaces"></a>Podporované rozhraní
### <a name="opos"></a>OPOS

K zajištění, že největší rozsah zařízení lze použít s Microsoft Dynamics 365 pro operace - maloobchod, OLE pro standardní POS je primární maloobchodní periferní zařízení platforma, která je podporována v 365 Microsoft Dynamics pro operace - maloobchod. OLE pro POS standard byl vytvořen tak, že vnitrostátní maloobchodní federace (NRF), kterým se stanoví standardní komunikační protokoly pro maloobchodní periferní zařízení. OPOS je široce přijímaná implementace OLE pro POS standard. Byl vyvinut v mid-1990s a aktualizoval několikrát od té doby. OPOS poskytuje Architektura ovladače zařízení, který umožňuje snadnou integraci POS hardwaru se systémem Windows POS systémy. OPOS řídí zpracování komunikace mezi kompatibilní hardware a software Retail POS. Ovládací prvek OPOS se skládá ze dvou částí:

-   **Objekt Control** – objekt řízení u určité třídy zařízení (například řádek zobrazí) poskytuje rozhraní pro softwarový program. Služby konzultace Monroe ([www.monroecs.com](http://www.monroecs.com/)) poskytuje standardizovaný soubor OPOS ovládací prvek objekty, které jsou označovány jako objekty společných ovládacích prvků (CCOs). CCOs se používá k testování součást 365 Microsoft Dynamics pro operace - Retail POS. Proto testování pomáhá zaručit, že, pokud 365 Microsoft Dynamics pro operace - podporuje maloobchodní zařízení třídy prostřednictvím OPOS, mnoho typů zařízení mohou být podporovány, aby výrobce poskytuje služby objekt, který je sestaven pro OPOS. Není nutné explicitně testovat každý typ zařízení.
-   **Objekt služby** – objekt služby zajišťuje komunikaci mezi objekt control (CCO) a zařízení. Objekt služby pro zařízení obvykle pochází od výrobce zařízení. Nicméně v některých případech bude pravděpodobně nutné stáhnout z webu výrobce objektu služby. Například novější objekt služby mohou být k dispozici. Najít adresu na webu výrobce, naleznete v dokumentaci k hardwaru.

[![Ovládací prvek objektu a objekt služby](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) podpora pro provádění OLE OPOS POS pomáhá zaručit, že pokud zařízení výrobců a vydavatelů POS standard správně implementovat, Pokladních systémů a podporovaných zařízení mohou spolupracovat, i v případě, že nebyly testovány dříve společně. **Poznámka:** podporu OPOS nezaručuje podporu pro všechna zařízení, která mají ovladače OPOS. Microsoft Dynamics 365 pro operace - maloobchodní musí nejprve podporovat tento typ zařízení nebo třídy prostřednictvím OPOS. Kromě toho objektů služby nemusí být vždy aktuální s nejnovější verzí CCOs. Je třeba také věnovat pozornost, obecně kvalita objektů služby se liší.

### <a name="windows"></a>Systém Windows

Tisk účtenky v POS je optimalizována pro OPOS. OPOS má tendenci být mnohem rychlejší než tisk pomocí systému Windows. Je tedy vhodné použít OPOS, zejména v maloobchodním prostředí, kde 40 sloupci příjmy jsou vytištěny časy transakcí musí být rychlé. U většiny zařízení budete používat ovládací prvky OPOS. Některé tiskárny OPOS příjmu však podporují ovladače systému Windows. Pomocí ovladače Windows dostanete nejnovější písma a jednu tiskárnu sítě pro více registrů. Existují však nevýhody použití ovladačů systému Windows. Zde jsou některé příklady těchto nevýhod:

-   Při použití ovladače Windows obrázky jsou vykreslovány před tiskem. Proto tisk má tendenci být pomalejší než u tiskáren, které používají ovládací prvky OPOS.
-   Zařízení, která jsou připojena prostřednictvím tiskárny ("sedmikráska chain") nemusí správně fungovat při použití ovladače Windows. Například nemusí otevřít zásuvku nebo slip tiskárny nemusí word podle očekávání.
-   OPOS podporuje také rozsáhlejší sady proměnných, které jsou specifické pro maloobchodní příjmu, jako například tiskárny tisk složenky nebo řezání papíru.

Pokud OPOS ovládací prvky jsou k dispozici pro tiskárny systému Windows, kterou používáte, tiskárna by stále pracovat správně s 365 Microsoft Dynamics pro operace - Retail.

### <a name="universal-windows-platform"></a>Universal Windows Platform

UWP, v případě maloobchodní periferní zařízení, se vztahuje na podporu systému Windows pro zařízení Plug and Play. Zařízení Plug and Play připojen na verzi operačního systému Windows, který podporuje typ zařízení, je nutné zařízení používané jako určen žádný ovladač. Například, pokud systém Windows rozpozná zařízení Bluetooth reproduktor, operační systém ví, že zařízení má **reproduktor** typ třídy. Proto a toto zařízení se považuje za lektorem. Není zapotřebí žádné další nastavení. V případě POS zařízení zapojit mnoho zařízení USB a systém Windows je rozpozná jako zařízení standardu HID (HIDs). Však nemusí být schopni určit možnosti, které poskytuje zařízení, protože zařízení neurčuje třídu nebo typ zařízení. V systému Windows 10 byly přidány třídy zařízení pro skenery čárového kódu a MSRs. Proto pokud zařízení prohlašuje, že na Windows 10 jako jedné z těchto tříd zařízení, systém Windows bude naslouchat události ze zařízení ve vhodných okamžicích. Moderní POS podporuje UWP MSRs a skenery. Proto když je připraven pro vstup z jednoho z těchto zařízení a zařízení, které patří do jedné z těchto tříd je připojen, lze použít zařízení. Například pokud je připojen počítač Windows 10 UWP bar kód skener a čárový kód přihlášení je nakonfigurován pro moderní POS, čtečka čárového kódu je aktivní na přihlašovací obrazovce. Není zapotřebí žádné další nastavení. Další třídy point service UWP zařízení jsou přidávány do systému Windows. Tyto třídy zahrnují třídy pro zásuvky a příjmu tiskárny. Podpora pro tyto nové třídy zařízení v moderní POS čeká na vyřízení.

### <a name="keyboard-wedge"></a>Klávesnice wedge

Zařízení klávesnice wedge odeslat data do počítače, jako by data byla zadána na klávesnici. Proto ve výchozím nastavení, pole, který je aktivní v POS obdrží data, která je naskenované nebo protažené. V některých případech toto chování může způsobit nesprávný typ dat, které mají být prohledány v nesprávném poli. Například může prohledávat čárového kódu do pole, které je určeno k zadání údajů platební karty. V mnoha případech je logika v POS, která určuje, zda data, která je naskenované nebo protažené čárový kód nebo protažení karty. Proto je správně zpracovat data. Je-li zařízení nastaveno jako OPOS místo klávesnice wedge zařízení, existuje však větší kontrolu nad jak data z těchto zařízení mohou být spotřebovány, protože více je "známý" o zařízení, které data pocházejí od. Například data ze skeneru čárového kódu automaticky rozpoznána jako čárový kód a snadněji a rychleji, než pokud byly použity obecný řetězec hledání, jako v případě klávesnice wedge zařízení nalezen přidružený záznam v databázi.

### <a name="native-printer"></a>Nativní tiskárny

Nativní (nebo v hardwarovém profilu se nazývá "Zařízení" jako typ) tiskárny lze nakonfigurovat tak, aby výzvu k výběru tiskárny, který je nakonfigurován pro počítač. Pokud tiskárně **zařízení** typ je nakonfigurován, pokud moderní POS narazí příkaz pro tisk, bude uživatel vyzván k výběru tiskárny v seznamu. Toto chování se liší od chování ovladačů pro systém Windows, protože **Windows** typ tiskárny hardwarový profil nezobrazí seznam tiskáren. Místo toho vyžaduje být součástí tiskárny s názvem **název zařízení** pole.

### <a name="windows"></a>Systém Windows

**Windows** typu zařízení se používá pro pouze tiskárny. Pokud tiskárny systému Windows je nakonfigurován v hardwarovém profilu, je třeba zadat název konkrétní tiskárny. Když moderní POS setká tiskové události, pokud je nakonfigurován tiskárny systému Windows, události budou předány zadané tiskárny systému Windows. Uživatel nebude vyzván výběr tiskárny.

### <a name="network"></a>Síť

V síti přímo hardware stanice meziprocesová komunikace (IPC), která je integrována v moderní POS pro aplikace systému Windows nebo pomocí stanice hardwaru služby IIS pro ostatní klienty moderní POS lze adresovat síťové zásuvky tiskárny příjmu a platební terminály.

## <a name="hardware-station-deployment-options"></a>Možnosti nasazení hardwaru stanice
### <a name="ipc-built-in"></a>IPC (předdefinovaná)

Hardwarová stanice meziprocesová komunikace (IPC) je součástí moderní POS pro aplikace systému Windows. Chcete-li použít hardware stanice IPC, přiřazení profilu hardwaru do registru, který bude používat moderní POS pro aplikace systému Windows. Pak vytvořte hardware stanice **Dedicated** typ úložiště použití registru. Při spuštění moderní POS hardwaru stanice IPC bude aktivní a POS periferie, které byly nakonfigurovány bude připraven k použití. Pokud z nějakého důvodu dočasně není vyžadují místní hardware, použijte **spravovat hardware stanice** operace vypnutí hardwarové možnosti stanice. Moderní POS můžete také použít hardware stanice IPC přímo komunikovat s periferním zařízením v síti.

### <a name="iis"></a>služba IIS,

Můžete použít službu IIS nebo samostatnou verzi hardware stanice dvěma způsoby. Popisovač "IIS" znamená, že POS aplikace připojí k hardware stanice prostřednictvím Internetová informační služba. Aplikace POS připojuje stanice hardwaru služby IIS prostřednictvím webové služby, které jsou spuštěny v počítači, kde jsou zařízení připojená. Při použití služby IIS lze použít maloobchodní periferní zařízení, které jsou připojeny k hardware stanice podle jakékoli Pokladna POS, který je ve stejné síti jako hardware stanice služby IIS. Protože pouze moderní POS for Windows obsahuje integrovanou podporu pro maloobchodní periferní zařízení, všechny ostatní aplikace moderních POS použít hardware stanice služby IIS ke komunikaci s POS periferie, které jsou nakonfigurovány v hardwarovém profilu. Proto každé instance služby IIS hardware stanice vyžaduje počítač, který spustí webové služby a aplikace, která komunikuje s zařízení. Hardwarová stanice služby IIS je vyžadována pro všechny non - Windows moderní POS aplikace.

#### <a name="dedicated"></a>Vyhrazeno

Moderní POS používá hardware stanice **Dedicated** typu ke zjištění, že periferní zařízení jsou přímo připojeny k počítači, kde je používána aplikace. Však **Dedicated** typ lze použít také pro hardware stanice služby IIS. V tradiční, pevné POS scénář, který používá Cloud POS jako aplikace Retail POS **Dedicated** stanice typu hardwaru se používá pro hardware stanice služby IIS, které jsou nasazeny ve stejném počítači, je systémem shluk POS. Z hlediska maloobchodní periferní zařízení lépe maloobchodní vyhrazené hardwarové stanice IIS periferní podpora pro tradiční pevné scénáře POS. Vyhrazené hardwarové stanice podporují všechna periferní zařízení, které jsou podporovány v hardwarovém profilu.

#### <a name="shared"></a>Sdílený

Sdílet hardware stanice jsou určeny pro více zařízení POS až v průběhu dne. Sdílený hardware, který stanice jsou optimalizovány pro podporu pouze zásuvky, příjem tiskárny a platební terminály. Nelze přímo připojit samostatný čárový kód skenery, MSRs, řádek zobrazí, nastaví nebo jiná zařízení. Jinak bude dojít ke konfliktům při deklarace těchto periferních zařízení současně více zařízení POS. Zde je způsob správy konfliktů u podporovaných zařízení:

-   **Zásuvku** – zásuvku je otevřen prostřednictvím událostí, který je odeslán do zařízení. Jediný problém, který může dojít, pokud je volána hotovostí nastane, pokud zásuvku je již otevřen. V případě sdíleného hardware stanice by měla být nastavena zásuvku **sdílené** v hardwarovém profilu. Toto nastavení zabrání kontrole, zda zásuvku již otevřen při odešle příkazy Otevřít POS.
-   **Příjem tiskárny** -Pokud dva příjem tiskové příkazy jsou odesílány hardware stanice současně, jeden z příkazů můžete ztratit, v závislosti na zařízení. Některá zařízení mají interní paměť nebo fondy, které může zabránit tomuto problému. Pokud tiskový příkaz není úspěšný, pokladník obdrží chybovou zprávu a můžete opakovat příkaz pro tisk z programu POS.
-   **Terminálové platby** -pokud pokladník snaží řízení transakce na terminálu platbu, která je již používán, zprávy upozorní pokladník, že terminál je používán a požádá pokladník akci později. Pokladníci obvykle zjistí, že terminál je již používán a bude čekat, dokud dokončení jiné transakce předtím, než se pokusí znovu řízení.

Ověření je plánováno pro budoucí verze, chcete-li zjistit, zda jsou nastaveny nepodporované zařízení v hardwarovém profilu, který je mapován na sdílené hardware stanice. Pokud jsou zjištěny všechny nepodporované zařízení, uživatel obdrží zprávu, která uvádí, že zařízení nejsou podporovány pro sdílené hardware stanice. V případě sdíleného hardware stanice **vybrat na základě nabídkového řízení** možnost nastavena na **Ano** na úrovni registru. Uživatel POS je potom výzva k výběru hardware stanice při výběru nabídky pro transakce v POS. Vybráno hardwarové stanice pouze v době vyhlášení výběr hardware stanice přidá přímo do pracovního postupu POS pro mobilní scénáře. Další výhodou zobrazení řádku Terminálové platby nepoužívá sdílené scénáře. Pokud Terminálové platby slouží jako zobrazení řádku, ostatní uživatelé mohou být blokovány z používání tohoto terminálu, dokud transakce neskončí. V mobilní scénáře mohou být přidány řádky transakce za delší období. Proto **vybrat na základě nabídkového řízení** možnost je vyžadována k zajištění dostupnosti zařízení optimální.

### <a name="network-peripherals"></a>Síťové příslušenství

Označení síťové zařízení v hardwarovém profilu umožňuje zásuvky, příjem tiskárny a platební terminály připojit prostřednictvím připojení k síti.

#### <a name="modern-pos-for-windows"></a>Moderní POS pro systém Windows

Můžete určit adresy IP síťového příslušenství na dvou místech. Pokud klient systému Windows moderní POS používá jednu sadu společnosti network peripherals, měli byste nastavit adresy IP těchto zařízení pomocí **konfigurace IP** možnosti v podokně akcí pro registrační pokladnu sama. U síťových zařízení, které budou sdíleny mezi Registry POS hardwarový profil, který má přiřazena síťovým zařízením lze mapovat přímo na sdílený hardware stanice. Přiřadit adresy IP, vyberte tento hardware stanice na **maloobchodní obchody** stránku a potom použít **konfigurace IP** možnost **Hardware stanice** sekce určit síťová zařízení, které jsou přiřazeny k dané hardwarové stanice. Pro hardware stanice, které mají pouze síťová zařízení nemusíte instalovat hardware stanice sám. V tomto případě hardware stanice je nezbytný pouze při koncepčně skupiny sítě adresovatelné zařízení podle jejich umístění v kamenném obchodě.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Moderní POS pro Android, Retail POS a moderní POS pro iOS v cloudu

Logika, která periferní zařízení fyzicky připojen a adresovat síťové jednotky jsou obsaženy v hardware stanice. Proto pro všechny klienty POS s výjimkou moderní POS pro systém Windows, hardware stanice služby IIS musí být nasazené a aktivní povolení POS periferie, bez ohledu na to, zda jsou tyto periferní zařízení fyzicky připojena k hardwaru stanice nebo určena v síti komunikovat.

## <a name="setup-and-configuration"></a>Nastavení a konfigurace
### <a name="hardware-station-installation"></a>Instalace hardwaru stanice

Informace naleznete v tématu [maloobchodní hardwarové stanice konfiguraci a instalaci](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Moderní POS pro instalaci systému Windows a konfigurace

Informace naleznete v tématu [instalace a konfigurace programu Retail POS moderní](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>Konfigurace a instalace zařízení OPOS

Další informace o součástech OPOS naleznete v části "Podporované rozhraní" tohoto dokumentu. Obvykle se ovladače OPOS poskytnuté výrobcem zařízení. Pokud je nainstalován ovladač zařízení OPOS, přidává klíč registru systému Windows v jednom z následujících umístění:

-   **32bitový systém:** HKEY\_místní\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64bitový systém:** HKEY\_místní\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

V klíči registru ServiceOPOS konfigurované zařízení jsou uspořádány podle třídy zařízení OPOS. Více ovladačů zařízení jsou uloženy.

## <a name="supported-scenarios-by-hardware-station-type"></a>Podporované scénáře podle typu hardwaru stanice
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Podpora klientů – IPC hardware stanice vs. IIS hardware stanice

V následující tabulce jsou uvedeny topologie a scénářů nasazení, které jsou podporovány.

| Klient      | Hardwarová stanice IPC | Služba IIS hardware stanice |
|-------------|----------------------|----------------------|
| Aplikace systému Windows | Ano                  | Ano                  |
| Shluk POS   | Žádný                   | Ano                  |
| Android     | Žádný                   | Ano                  |
| iOS         | Žádný                   | Ano                  |

### <a name="network-peripherals"></a>Síťové příslušenství

Přímo přes hardware stanice, která je integrována v moderní POS pro aplikace systému Windows mohou být podporovány společnosti Network peripherals. Pro ostatní klienty je nutné nasadit služby IIS hardware stanice.

| Klient      | Hardwarová stanice IPC | Služba IIS hardware stanice |
|-------------|----------------------|----------------------|
| Aplikace systému Windows | Ano                  | Ano                  |
| Shluk POS   | Žádný                   | Ano                  |
| Android     | Žádný                   | Ano                  |
| iOS         | Žádný                   | Ano                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Podporované typy zařízení podle typu hardwaru stanice
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderní POS pro systém Windows pomocí hardware stanice IPC (předdefinovaná)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Podporovaná zařízení třídy</th>
<th>Podporované rozhraní</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tiskárna</td>
<td><ul>
<li>OPOS</li>
<li>Ovladač systému Windows</li>
<li>Zařízení</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="even">
<td>Tiskárna 2</td>
<td><ul>
<li>OPOS</li>
<li>Ovladač systému Windows</li>
<li>Zařízení</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="odd">
<td>Řádkový displej</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Duální displej</td>
<td>Ovladač systému Windows</td>
</tr>
<tr class="odd">
<td>MSR</td>
<td><ul>
<li>OPOS</li>
<li>UWP (není vyžadováno žádné nastavení.)</li>
<li>Klávesnice wedge (není vyžadováno žádné nastavení.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Výstavce</td>
<td><ul>
<li>OPOS</li>
<li>Síťové <strong>Poznámka:</strong> pouze jednu zásuvku lze nastavit v případě <strong>použití sdílených shift</strong> nastaven na zásuvky.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zásuvka 2</td>
<td><ul>
<li>OPOS</li>
<li>Síťové <strong>Poznámka:</strong> pouze jednu zásuvku lze nastavit v případě <strong>použití sdílených shift</strong> nastaven na zásuvky.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skener</td>
<td><ul>
<li>OPOS</li>
<li>UWP (není vyžadováno žádné nastavení.)</li>
<li>Klávesnice wedge (není vyžadováno žádné nastavení.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skener 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (není vyžadováno žádné nastavení.)</li>
<li>Klávesnice wedge (není vyžadováno žádné nastavení.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Měřítko</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Klávesnice pro kód PIN</td>
<td>OPOS (podpora je poskytována prostřednictvím vlastní konektor platby).</td>
</tr>
<tr class="even">
<td>Zaznamenání podpisu</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Patební terminál </td>
<td><ul>
<li>Podpora vlastního zařízení</li>
<li>Síti (Další informace naleznete v dokumentaci konektor platby.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Všechny moderní POS klienty, kteří mají vyhrazené hardwarové stanice služby IIS

**Poznámka:** při IIS hardware stanice "vyhrazen," je vztah 1: 1 mezi klientem POS a hardware stanice.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Podporovaná zařízení třídy</th>
<th>Podporované rozhraní</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tiskárna</td>
<td><ul>
<li>OPOS</li>
<li>Ovladač pro systém Windows <strong>Poznámka:</strong> pro Windows tiskárny v síti, uživatel hardware stanice musí mít oprávnění k přístupu k tiskárně.</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="even">
<td>Tiskárna 2</td>
<td><ul>
<li>OPOS</li>
<li>Ovladač systému Windows</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="odd">
<td>Řádkový displej</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>MSR</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Výstavce</td>
<td><ul>
<li>OPOS</li>
<li>Síťové <strong>Poznámka:</strong> pouze jednu zásuvku na hardwarovém profilu lze nastavit v případě <strong>použití sdílených shift</strong> nastaven na zásuvky.</li>
</ul></td>
</tr>
<tr class="even">
<td>Zásuvka 2</td>
<td><ul>
<li>OPOS</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skener</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Skener 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Měřítko</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Klávesnice pro kód PIN</td>
<td>OPOS (podpora je poskytována prostřednictvím vlastní konektor platby).</td>
</tr>
<tr class="odd">
<td>SIG. zachycení</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Patební terminál </td>
<td><ul>
<li>Podpora vlastního zařízení</li>
<li>Síti (Další informace naleznete v dokumentaci konektor platby.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Všechny moderní POS klienty, kteří mají hardware stanice sdílené služby IIS

**Poznámka:** při IIS hardware stanice je "sdílení" více zařízení lze použít hardware stanice ve stejnou dobu. V tomto scénáři byste měli použít pouze zařízení, které jsou uvedeny v následující tabulce. Pokud se pokusíte sdílet zařízení, které zde nejsou uvedeny, jako jsou skenery čárového kódu a MSRs, dojde k chybám při více zařízení nárokovat stejné periferie. V budoucnu taková konfigurace explicitně moci.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Podporovaná zařízení třídy</th>
<th>Podporované rozhraní</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tiskárna</td>
<td><ul>
<li>OPOS</li>
<li>Ovladač pro systém Windows <strong>Poznámka:</strong> pro Windows tiskárny v síti, uživatel hardware stanice musí mít oprávnění k přístupu k tiskárně.</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="even">
<td>Tiskárna 2</td>
<td><ul>
<li>OPOS</li>
<li>Ovladač systému Windows</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="odd">
<td>Výstavce</td>
<td><ul>
<li>OPOS</li>
<li>Síťové <strong>Poznámka:</strong> pouze jednu zásuvku na hardwarovém profilu lze nastavit v případě <strong>použití sdílených shift</strong> nastaven na zásuvky.</li>
</ul></td>
</tr>
<tr class="even">
<td>Zásuvka 2</td>
<td><ul>
<li>OPOS</li>
<li>Síť</li>
</ul></td>
</tr>
<tr class="odd">
<td>Patební terminál </td>
<td><ul>
<li>Podpora vlastního zařízení</li>
<li>Síti (Další informace naleznete v dokumentaci konektor platby.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfigurace pro podporované scénáře
Další informace o vytváření hardwarových profilů naleznete v tématu [definovat a udržovat kanál klientů, včetně registrů a hardware stanice](define-maintain-channel-clients-registers-hw-stations.md). **Poznámka:** pro Microsoft Dynamics 365 pro verzi operace 1611, hardwarový profil stanice již není používán. Atributy, které jste nastavili v hardwarovém profilu stanice jsou nyní součástí hardware stanice sám.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderní POS pro systém Windows pomocí hardware stanice IPC (předdefinovaná)

Tato konfigurace je nejtypičtější konfiguraci pro tradiční, pevné Registry POS. V tomto scénáři je informace v profilu hardwaru mapovány přímo na samotný registr. Číslo terminálu EFT by měl také nastavit v registru sám. Chcete-li nastavit tuto konfiguraci, postupujte takto.

1.  Vytvoření hardwarového profilu, kde jsou nakonfigurovány všechny požadované periferie.
2.  Mapovat Pokladna POS hardwarový profil.
3.  Vytvořit hardwarové stanice **Dedicated** typ maloobchodu použití Pokladna POS. Popis je nepovinný. **Poznámka:** nemáte, chcete-li nastavit další vlastnosti na stanici hardwaru. Všechny další požadované informace, například profil hardwaru budou pocházet z rejstříku sám.
4.  Klepněte na tlačítko **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**.
5.  Vyberte **1090** plán distribuce synchronizovat nový hardwarový profil do úložiště. Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny POS.
6.  Vyberte **1040** plán distribuce synchronizovat nový hardware stanice do úložiště. Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny POS.
7.  Instalace a aktivace moderní POS pro systém Windows.
8.  Moderní POS pro systém Windows spustit a začít používat připojená periferní zařízení.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Všechny moderní POS klienty, kteří mají vyhrazené hardwarové stanice služby IIS

Tuto konfiguraci lze použít pro všechny klienty moderní POS, které mají hardware stanice, která používá výhradně jeden POS zaregistrovat. Chcete-li nastavit tuto konfiguraci, postupujte takto.

1.  Vytvoření hardwarového profilu, kde jsou nakonfigurovány všechny požadované periferie.
2.  Vytvořit hardwarové stanice **Dedicated** typ maloobchodu použití Pokladna POS.
3.  Vyhrazené hardwarové stanice nastavte následující vlastnosti:
    -   **Název hostitele** – název hostitelského počítače, kde bude spuštěn hardwaru stanice. **Poznámka:** Cloud POS lze vyřešit **localhost** k určení místního počítače, kde běží Cloud POS. Však certifikát, který je nutný pro Cloud POS spárovat hardware stanice musí mít také "Localhost" jako název počítače. Chcete-li zabránit problémům, doporučujeme seznamu instance každé vyhrazené hardwarové stanice pro obchod, jak je požadováno. Pro každé hardwarové stanice hostitele název by měl být název konkrétního počítače kde budou nasazeny hardwarové stanice.
    -   **Port** – port, který chcete použít ke komunikaci s klientem moderní POS hardwaru stanice.
    -   **Hardwarový profil** -Pokud není hardwarový profil, pokud hardware stanice sám, bude použit hardwarový profil, který je přiřazen k rejstříku.
    -   **Číslo EFT POS** – ID terminálu EFT při povolení EFT jsou odesílány. Toto ID je k dispozici procesoru platební karty.
    -   **Název balíčku** – balíček hardware stanice pro použití při nasazení hardwaru stanice.

4.  Klepněte na tlačítko **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**.
5.  Vyberte **1090** plán distribuce synchronizovat nový hardwarový profil do úložiště. Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny POS.
6.  Vyberte **1040** plán distribuce synchronizovat nový hardware stanice do úložiště. Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny POS.
7.  Nainstalujte hardware stanice. Další informace o instalaci hardwaru stanice, viz [maloobchodní hardwarové stanice konfiguraci a instalaci](retail-hardware-station-configuration-installation.md).
8.  Instalace a aktivace moderní POS. Další informace o instalaci moderní POS naleznete v tématu [instalace a konfigurace programu Retail POS moderní](retail-modern-pos-device-activation.md).
9.  Přihlášení do moderní POS a vyberte **provádět operace bez zásuvky**.
10. Start **spravovat hardware stanice** operace.
11. Klepněte na tlačítko **Správa**.
12. Na stránce Správa hardwaru stanice nastavte možnost zapnout hardware stanice.
13. Vyberte hardware stanice a potom klepněte na tlačítko **pár**.
14. Poté, co je spárováno stanice hardwaru, klepněte na tlačítko **Zavřít**.
15. Na stránce Výběr stanice hardware klepněte na naposledy vybraný hardwarový stanice na aktivní.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Všechny moderní POS klienty, kteří mají hardware stanice sdílené služby IIS

Tuto konfiguraci lze použít pro všechny klienty moderní POS, které sdílejí hardware stanice s jinými zařízeními. Chcete-li nastavit tuto konfiguraci, postupujte takto.

1.  Vytvoření hardwarového profilu, kde jsou nakonfigurovány požadované příslušenství.
2.  Vytvořit hardwarové stanice **sdílené** typ maloobchodu použití Pokladna POS.
3.  Na stanici sdílený hardware nastavte následující vlastnosti:
    -   **Název hostitele** – název hostitelského počítače, kde bude spuštěn hardwaru stanice.
    -   **Popis** – Text, který pomůže identifikovat hardware stanice, jako například **vrátí** nebo **přední úložiště**.
    -   **Port** – port, který chcete použít ke komunikaci s klientem moderní POS hardwaru stanice.
    -   **Hardwarový profil** – pro sdílený hardware stanice by měl mít každý hardware stanice hardwarový profil. Hardwarové profily lze sdílet mezi stanicemi hardware, ale musí být mapována na každé stanici hardwaru. Kromě toho doporučujeme použít sdílené směny, použijete-li více zařízení stejného sdíleného hardware stanice. Nastavit sdílené shift, klepněte na tlačítko **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily**. Pro každý sdílený hardwarový profil vyberte zásuvku a nastavte **zásuvku sdílených shift** možnost na **Ano**.
    -   **Číslo EFT POS** – ID terminálu EFT při povolení EFT jsou odesílány. Toto ID je k dispozici procesoru platební karty.
    -   **Název balíčku** – balíček hardware stanice pro použití při nasazení hardwaru stanice.

4.  Opakujte kroky 2 a 3 pro každý další hardware stanice, který je vyžadován v úložišti.
5.  Klepněte na tlačítko **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**.
6.  Vyberte **1090** plán distribuce synchronizovat nový hardwarový profil do úložiště. Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny POS.
7.  Vyberte **1040** plán distribuce synchronizovat nový hardware stanice do úložiště. Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny POS.
8.  Nainstalujte hardware stanice každý hostitelský počítač, který jste vytvořili v krocích 2 a 3. Další informace o instalaci hardwaru stanice, viz [maloobchodní hardwarové stanice konfiguraci a instalaci](retail-hardware-station-configuration-installation.md).
9.  Instalace a aktivace moderní POS. Další informace o instalaci moderní POS naleznete v tématu [instalace a konfigurace programu Retail POS moderní](retail-modern-pos-device-activation.md).
10. Přihlášení do moderní POS a vyberte **provádět operace bez zásuvky**.
11. Start **spravovat hardware stanice** operace.

12. Klepněte na tlačítko **Správa**.
13. Na stránce Správa hardwaru stanice nastavte možnost zapnout hardware stanice.
14. Vyberte hardware stanice a potom klepněte na tlačítko **pár**.
15. Krok 14 zopakujte pro každé hardwarové stanice, která bude používat moderní POS.
16. Jakmile jsou spárovány všechny stanice potřebný hardware, klepněte na tlačítko **Zavřít**.
17. Na stránce Výběr stanice hardware klepněte na naposledy vybraný hardwarový stanice na aktivní. **Poznámka:** Pokud zařízení často používají různé hardwarové stanice, doporučujeme nakonfigurovat v moderní POS výzvy pokladníci po jejich zahájení procesu úhrady vyberte hardware stanice. Klepněte na tlačítko **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**registruje**. Vyberte registr a poté nastavte **na nabídku vyberte** možnost na **Ano**. Použití **1090** plán distribuce synchronizovat změny databáze kanálů.

## <a name="extensibility"></a>Rozšiřitelnost
Informace o scénářích rozšiřitelnosti pro hardware stanice naleznete v tématu [rozšíření Hardware stanice](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Zabezpečení
Podle aktuální bezpečnostní normy měla používat následující nastavení v produkčním prostředí: **Poznámka:** instalační program hardwaru stanice automaticky provést tyto úpravy registru jako součást instalace prostřednictvím samoobslužné služby.

-   Protokol SSL (Secure Sockets Layer) (SSL) by mělo být zakázáno.
-   Pouze zabezpečení TLS (Transport Layer) verze 1.2 (nebo aktuální nejvyšší) je povolena a používá. **Poznámka:** ve výchozím nastavení, SSL a všechny verze s výjimkou TLS 1.2 TLS jsou zakázány. Chcete-li upravit nebo povolit tyto hodnoty, postupujte takto:
    1.  Stiskněte klávesu s logem Windows key + R otevřete **spuštění** okna.
    2.  V **Open** pole, zadejte **Regedit**a potom klepněte na tlačítko **OK**.
    3.  Pokud **řízení uživatelských účtů** okno se zprávou se zobrazí, klepněte na tlačítko **Ano**.
    4.  V **Editor registru** okna, přejděte na **HKEY\_místní\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Následující klávesy byli jste automaticky zařazeni pouze povolit protokol TLS 1.2:
        -   TLS 1.2Server: povoleno = 1
        -   TLS 1.2Server:DisabledByDefault = 0
        -   TLS 1.2Client: povoleno = 1
        -   TLS 1.2Client:DisabledByDefault = 0
        -   TLS 1.1Server: povoleno = 0
        -   TLS 1.1Client: povoleno = 0
        -   TLS 1.0Server: povoleno = 0
        -   TLS 1.0Client: povoleno = 0
        -   SSL 3.0Server: povoleno = 0
        -   SSL 3.0Client: povoleno = 0
        -   SSL 2.0Server: povoleno = 0
        -   SSL 2.0Client: povoleno = 0
-   Žádné další síťové porty musí být otevřené, pokud jsou vyžadovány z důvodu známé, zadaný.
-   Sdílení zdrojů mezi původu musí být zakázána a určit povolený původu, které byly přijaty.
-   Pouze důvěryhodné certifikační úřady by měla sloužit k získání certifikátů, které budou použity v počítačích se systémem hardware stanice.

**Poznámka:** je velmi důležité zkontrolovat bezpečnostní pokyny pro služby IIS a požadavky na platební karty Industry (PCI).

## <a name="peripheral-simulator"></a>Simulátor periferních zařízení
Informace naleznete v tématu [maloobchodní periferní simulátor](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Periferní zařízení Microsofttested
### <a name="ipc-built-in-hardware-station"></a>Hardwarová stanice IPC (předdefinovaná)

Následující příslušenství byly testovány pomocí stanice IPC hardware, který je integrován v moderní POS pro systém Windows.

#### <a name="printer"></a>Tiskárna

| Výrobce | Model    | Rozhraní | Poznámky                |
|--------------|----------|-----------|-------------------------|
| Tiskárny EPSON        | TM-T88IV | OPOS      |                         |
| Tiskárny EPSON        | TM-T88V  | OPOS      |                         |
| Hvězda         | TSP650II | OPOS      |                         |
| Hvězda         | TSP650II | Vlastní    | Připojení prostřednictvím sítě   |
| Hvězda         | mPOP     | OPOS      | Připojen pomocí Bluetooth |
| HP           | F7M67AA  | OPOS      | Napájení USB             |

#### <a name="bar-code-scanner"></a>Skener čárových kódů

| Výrobce  | Model         | Rozhraní | Poznámky |
|---------------|---------------|-----------|----------|
| Společnost Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Symbol        | LS2208        | OPOS      |          |
| HP integrovaný | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>Klávesnice pro kód PIN

| Výrobce | Model  | Rozhraní | Poznámky                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Vyžaduje vlastní konektor platby |

#### <a name="payment-terminal"></a>Patební terminál 

| Výrobce | Model | Rozhraní | Poznámky                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Vlastní    | Vyžaduje vlastní konektor platby                                |
| VeriFone     | MX925 | Vlastní    | Vyžaduje vlastní konektor platby; připojit prostřednictvím sítě a USB |
| VeriFone     | MX915 | Vlastní    | Vyžaduje vlastní konektor platby; připojit prostřednictvím sítě a USB |

#### <a name="cash-drawer"></a>Zásuvku

| Výrobce | Model     | Rozhraní | Poznámky                |
|--------------|-----------|-----------|-------------------------|
| Hvězda         | mPOP      | OPOS      | Připojen pomocí Bluetooth |
| APG          | Atwood    | Vlastní    | Připojení prostřednictvím sítě   |
| Hvězda         | SMD2 1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Řádkový displej

| Výrobce  | Model   | Rozhraní | Poznámky |
|---------------|---------|-----------|----------|
| HP integrovaný | G6U79AA | OPOS      |          |
| Tiskárny EPSON         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Zaznamenání podpisu

| Výrobce | Model  | Rozhraní | Poznámky |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Měřítko

| Výrobce | Model         | Rozhraní | Poznámky |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Výrobce | Model       | Rozhraní | Poznámky |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Vyhrazené hardwarové stanice služby IIS

Následující příslušenství byly testovány pomocí vyhrazené (nesdíleném) hardware stanice IIS spolu s moderní POS pro systém Windows a Cloud POS.

#### <a name="printer"></a>Tiskárna

| Výrobce | Model    | Rozhraní | Poznámky                  |
|--------------|----------|-----------|---------------------------|
| Tiskárny EPSON        | TM-T88IV | OPOS      |                           |
| Tiskárny EPSON        | TM-T88V  | OPOS      |                           |
| Hvězda         | TSP650II | OPOS      |                           |
| Hvězda         | TSP650II | Vlastní    | Připojení prostřednictvím sítě     |
| Hvězda         | TSP100   | OPOS      | Vyžaduje ovladače TSP650II |
| HP           | F7M67AA  | OPOS      | Napájení USB               |

#### <a name="bar-code-scanner"></a>Skener čárových kódů

| Výrobce  | Model   | Rozhraní | Poznámky |
|---------------|---------|-----------|----------|
| Společnost Motorola      | DS9208  | OPOS      |          |
| Symbol        | LS2208  | OPOS      |          |
| HP integrovaný | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>Klávesnice pro kód PIN

| Výrobce | Model  | Rozhraní | Poznámky                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Vyžaduje vlastní konektor platby |

#### <a name="payment-terminal"></a>Patební terminál 

| Výrobce | Model | Rozhraní | Poznámky                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Vlastní    | Vyžaduje vlastní konektor platby                                |
| VeriFone     | MX925 | Vlastní    | Vyžaduje vlastní konektor platby; připojit prostřednictvím sítě a USB |
| VeriFone     | MX915 | Vlastní    | Vyžaduje vlastní konektor platby; připojit prostřednictvím sítě a USB |

#### <a name="cash-drawer"></a>Zásuvku

| Výrobce | Model     | Rozhraní | Poznámky              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Vlastní    | Připojení prostřednictvím sítě |
| Hvězda         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Řádkový displej

| Výrobce  | Model   | Rozhraní | Poznámky |
|---------------|---------|-----------|----------|
| HP integrovaný | G6U79AA | OPOS      |          |
| Tiskárny EPSON         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Zaznamenání podpisu

| Výrobce | Model  | Rozhraní | Poznámky |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Měřítko

| Výrobce | Model         | Rozhraní | Poznámky |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>MSR

| Výrobce | Model       | Rozhraní | Poznámky |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Sdílené služby IIS hardware stanice

Pomocí sdílené stanice hardwaru služby IIS a moderní POS pro systém Windows a Cloud POS byly testovány následující příslušenství. **Poznámka:** jsou podporovány pouze tiskárnu, Platební terminál a hotovostí.

#### <a name="printer"></a>Tiskárna

| Výrobce | Model    | Rozhraní | Poznámky                  |
|--------------|----------|-----------|---------------------------|
| Tiskárny EPSON        | TM-T88IV | OPOS      |                           |
| Tiskárny EPSON        | TM-T88V  | OPOS      |                           |
| Hvězda         | TSP650II | OPOS      |                           |
| Hvězda         | TSP650II | Vlastní    | Připojení prostřednictvím sítě     |
| Hvězda         | TSP100   | OPOS      | Vyžaduje ovladače TSP650II |
| HP           | F7M67AA  | OPOS      | Napájení USB               |

#### <a name="payment-terminal"></a>Patební terminál 

| Výrobce | Model | Rozhraní | Poznámky                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Vlastní    | Vyžaduje vlastní konektor platby; připojit prostřednictvím sítě a USB |
| VeriFone     | MX915 | Vlastní    | Vyžaduje vlastní konektor platby; připojit prostřednictvím sítě a USB |

#### <a name="cash-drawer"></a>Zásuvku

| Výrobce | Model     | Rozhraní | Poznámky              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Vlastní    | Připojení prostřednictvím sítě |
| Hvězda         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Řešení potíží
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Moderní POS můžete zjistit hardwarové stanice v seznamu pro výběr, ale nemůže dokončit párování

**Řešení:** zkontrolujte následující seznam možných bodů selhání:

-   Počítač se systémem moderní POS důvěřuje certifikátu, který se používá v počítači, který spouští hardware stanice.
    -   Chcete-li ověřit tato nastavení ve webovém prohlížeči přejděte na následující adresu URL: https://&lt;název počítače&gt;:&lt;číslo portu&gt;/HardwareStation/ping.
    -   Tuto adresu URL pomocí ping ověřte, zda je počítač přístupný a prohlížeče označuje, zda je certifikát důvěryhodný. (Například v aplikaci Internet Explorer ikonu zámku se zobrazí v adresním řádku. Klepnutím na tuto ikonu aplikace Internet Explorer ověří, zda je aktuálně důvěryhodný certifikát. Můžete nainstalovat certifikát místního počítače pomocí zobrazení Podrobnosti o certifikátu, který je zobrazen.)
-   V počítači, který spouští hardware stanice je v bráně firewall otevřít port použitý hardware stanice.
-   Hardwarová stanice byla nainstalována správně obchodní účet informace pomocí nástroje instalace obchodní informace, který spustí instalační program hardwaru stanice na konci.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Moderní POS nemůže rozpoznat hardware stanice v seznamu pro výběr

**Řešení:** tento problém může způsobit některá z následujících faktorů:

-   Hardwarová stanice nebyl nastaven správně v sídle. Ověřte správně zadán profil stanice hardwaru a hardwaru stanice pomocí kroků v tomto tématu.
-   Úlohy byly nespustili aktualizovat konfiguraci kanálu. V takovém případě spusťte úlohu 1070 pro konfiguraci kanálu.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Moderní POS neodráží nové nastavení pokladní zásuvky

**Řešení:** uzavření aktuální dávky. Moderní POS nejsou aktualizovány změny zásuvku do uzavření aktuální dávky.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Moderní POS hlásí problém s maloobchodní periferní

**Řešení:** Zde jsou některé obvyklé příčiny tohoto problému:

-   Ujistěte se, že další nástroje pro konfiguraci ovladače zařízení jsou zavřena. Pokud tyto nástroje jsou otevřeny, jejich může zabránit moderní POS nebo hardware stanice uplatňující zařízení.
-   Pokud je maloobchodní periferní sdílen s více POS zařízení, ujistěte se, že patří k jedné z následujících kategorií:
    -   Zásuvku
    -   Tiskárně stvrzenek
    -   Patební terminál 

    Pokud periferie nepatří do jedné z těchto kategorií, hardware stanice není určen povolení mají být sdíleny více zařízení POS periferie.
-   Ovladače zařízení může způsobit objekty společných ovládacích prvků (CCOs) přestal správně fungovat. Pokud zařízení nedávno nainstaloval, ale nepracuje správně nebo si všimnete jiné problémy, lze často vyřešit problém přeinstalací CCOs. Je možné stáhnout CCOs <http://monroecs.com/oposccos_current.htm>.
-   Pokud provádíte časté změny periferní během testování nebo řešení potíží, bude pravděpodobně nutné obnovit službu IIS namísto čekání sám aktualizovat mezipaměť. Chcete-li obnovit službu IIS, postupujte takto:
    1.  Z **spuštění** nabídky, typ **CMD**.
    2.  V okně Výsledky hledání klepněte pravým tlačítkem myši **příkazového řádku**a potom klepněte na tlačítko **spustit jako správce**.
    3.  V **příkazového řádku** okno, typ **příkaz iisreset/restart** a stiskněte klávesu Enter.
    4.  Moderní POS restartujte po restartování služby IIS.
-   Při periferní zařízení provádíte časté změny, pokud také často spustit a ukončit klienta POS, procesu dllhost z předchozí relace POS může rušit v aktuální relaci. Zařízení v tomto případě nemusí být použitelné až do zavření hostitele dynamická knihovna (DLL), který spravuje předchozí relace. Chcete-li zavřít hostiteli DLL, postupujte takto:
    1.  Z **spuštění** nabídky, typ **Správce úloh**.
    2.  V okně Výsledky hledání klepněte na tlačítko **Správce úloh**.
    3.  Ve Správci úloh na **podrobnosti** karta, klepněte na záhlaví sloupce, který je označen **jméno** Chcete-li seřadit tabulku abecedně podle názvu.
    4.  Přejděte dolů, dokud nenajdete dllhost.exe.
    5.  Vyberte každou DLL hostitele a potom klepněte na tlačítko **ukončit úlohu**.
    6.  Moderní POS restartujte zavření hostitelích DLL.


<a name="see-also"></a>Viz také
--------

[Maloobchodní periferní simulátor](retail-peripheral-simulator.md)




