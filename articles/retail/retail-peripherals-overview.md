---
title: "Přehled maloobchodních periferních zařízení"
description: "Toto téma vysvětluje pojmy související s maloobchodními periferními zařízeními."
author: rubencdelgado
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: ba9c828efc39d45a78500d30295e5d1d6c770c99
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="retail-peripherals-overview"></a>Přehled maloobchodních zařízení

[!include[banner](includes/banner.md)]


Toto téma vysvětluje pojmy související s maloobchodními periferními zařízeními. Popisuje různé způsoby, jakými mohou být periferní zařízení připojena k pokladnímu místu (POS) a komponenty odpovídající za správu připojení k POS.

## <a name="concepts"></a>Koncepty

### <a name="pos-registers"></a>Registry POS

Navigace: klikněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Pokladny**. Registr místa prodeje (POS) je entita, která se používá k definování vlastností konkrétní instance POS. Tyto vlastnosti zahrnují hardwarový profil nebo nastavení maloobchodních periferních zařízení, která budou použita na pokladně, obchod, ke kterému je pokladna namapována a vizuální prostředí uživatele, který se k dané pokladně přihlásí.

### <a name="devices"></a>Zařízení

Navigace: klikněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Zařízení**. Zařízení je entita, která představuje fyzickou instanci zařízení, která je namapována k pokladně POS. Při vytvoření je zařízení mapováno k pokladně POS. Zařízení sleduje informace o tom, kdy dojde k aktivaci pokladny POS, typu používaného klienta a balíčku aplikace, který byl nasazen na konkrétní zařízení. Zařízení lze mapovat na následující typy aplikací: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Windows Phone, Retail Modern POS – Android a Retail Modern POS – iOS.

### <a name="retail-modern-pos"></a>Moderní Retail POS

Modern POS je program POS pro systém Microsoft Windows. Může být nasazen v operačních systémech Windows 10.

### <a name="cloud-pos"></a>Cloud POS

Cloud POS je verze programu Modern POS pro prohlížeč, která je přístupná prostřednictvím webového prohlížeče.

### <a name="modern-pos-for-ios"></a>Modern POS pro iOS

Modern POS pro iOS je verze programu Modern POS založená na iOS, kterou lze implementovat na zařízeních se systémem iOS.

### <a name="modern-pos-for-android"></a>Modern POS pro Android

Modern POS pro Android je verze programu Modern POS založená na Androidu, kterou lze implementovat na zařízeních se systémem Android.

### <a name="pos-peripherals"></a>Periferní položky POS

Periferní položky POS jsou zařízení, která jsou explicitně podporována pro funkce POS. Tyto periferie jsou obvykle rozděleny do konkrétních tříd. Další informace o těchto třídách naleznete v části Třídy zařízení tohoto tématu.

### <a name="hardware-station"></a>Hardwarová stanice

Navigace: klikněte na **Retail** &gt; **Kanály** &gt; **Maloobchody** &gt; **Všechny maloobchody**. Vyberte obchod a potom klikněte na pevnou záložku **Hardwarové stanice**. Nastavení **hardwarové stanice** je nastavení na úrovni kanálu, které slouží k definování instancí, kde bude nasazena maloobchodní periferní logika. Toto nastavení na úrovni kanálů se používá k určení vlastností hardwarové stanice. Slouží také k výpisu hardwarových stanic, které jsou k dispozici pro instanci Modern POS v daném obchodě. Hardwarová stanice je součástí programu Modern POS for Windows. Hardwarovou stanici lze také nasadit nezávisle jako samostatný program Internetové informační služby (IIS) Microsoft. V tomto případě je přístupný prostřednictvím sítě.

### <a name="hardware-profile"></a>Profil hardwaru

Navigace: klikněte na **Maloobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Hardwarové profily**. Hardwarový profil je seznam zaříení, která jsou nakonfigurována pro pokladnu POS nebo hardwarovou stanici. Hardwarový profil lze přiřadit přímo k pokladně POS nebo k hardwarové stanici.

## <a name="devices-classes"></a>Třídy zařízení
Periferie POS jsou obvykle rozděleny do tříd. Tato část popisuje a poskytuje přehled zařízení, která podporuje Modern POS.

### <a name="printer"></a>Tiskárna

Tiskárny jsou tradiční tiskárny stvrzenek POS a tiskárny celých stránek. Tiskárny jsou podporovány prostřednictvím Object Linking and Embedding Retail POS (OPOS) a rozhraní ovladačů Microsoft Windows. Současně lze použít maximálně dvě tiskárny. Tato funkce umožňuje podporu scénářů, kdy se stvrzenky cash-and-carry pro zákazníky tisknou na tiskárnách strvzenek, zatímco objednávky zákazníků, které obsahují více informací, se tisknou na celostránkových tiskárnách. Tiskárny stvrzenek mohou být připojeny přímo k počítači pomocí USB, připojeny k síti přes Ethernet nebo připojeny přes Bluetooth.

### <a name="scanner"></a>Skener

Současně lze používat maximálně dva skenery čárových kódů. Tato funkce podporuje scénáře, kdy je nějaký skener, který je mobilnější, potřebný ke skenování velkých nebo těžkých položek, zatímco pevně uložený skener se používá pro většinu položek standardní velikosti pro urychlení doby rezervace. Skenery mohou být podporovány prostřednictvím OPOS, Universal Windows Platform (UWP) nebo rozhraní platebního terminálu klávesnice. Pro připojení skeneru k počítači lze použít USB nebo Bluetooth.

### <a name="msr"></a>MSR

Jednu USB čtečku magnetického proužku (MSR) lze nastavit pomocí ovladačů OPOS. Pokud chcete použít samostatnou čtečku MSR pro platební transakce elektronického převodu peněžních prostředků, musí být čtečka MSR spravována konektorem platby. Samostatné čtečky MSR lze použít pro věrnostní položku zákazníka, přihlášení zaměstnance a položku dárkového poukazu nezávisle na konektoru platby.

### <a name="cash-drawer"></a>Zásuvka s hotovostí

Na jeden profil hardwaru mohou být podporovány dvě zásuvky s hotovostí. Tato funkce umožňuje, aby jedné pokladně byly současně k dispozici dvě aktivní směny. V případě sdílené směny nebo v případě zásuvky s hotovostí, která je používána více mobilními zařízeními POS současně, je povolena pouze jedna zásuvka na jeden hardwarový profil. Zásuvky s hotovostí mohou být připojeny přímo k počítači pomocí USB, připojeny k síti nebo připojeny k tiskárně stvrzenek prostřednictvím rozhraní RJ12. V některých případech mohou být zásuvky s hotovostí připojeny také přes Bluetooth.

### <a name="line-display"></a>Řádkový displej

Řádkové displeje slouží k zobrazení produktů, částek transakcí a dalších užitečných informací zákazníkovi během transakce. K počítači lze prostřednictvím USB pomocí ovladače OPOS připojit jeden řádkový displej.

### <a name="signature-capture"></a>Zaznamenání podpisu

K počítači lze přes USB pomocí ovladače OPOS přímo připojit zařízení zaznamenání podpisu. Když bude nakonfigurován odběr podpisů, zákazník bude vyzván, aby se na zařízení podepsal. Po dodání podpisu bude podpis zobrazen pokladníkovi k přijetí.

### <a name="scale"></a>Měřítko

K počítači lze přes USP pomocí ovladače OPOS připojit váhu. Když bude k transakci přidán produkt označený jako "Vážený" produkt, POS odečte z váhy jeho hmotnost, přidá produkt k transakci a použije množství, které dodala váha.

### <a name="pin-pad"></a>Klávesnice pro kód PIN

Vložky na osobní identifikační číslo (PIN) jsou podporovány prostřednictvím OPOS, ale musí být spravovány prostřednictvím platebního konektoru.

### <a name="secondary-display"></a>Sekundární displej

Je-li nakonfigurován sekundární displej, bude k zobrazení základních informací používán displej Windows číslo 2. Účelem sekundárního displeje je podporovat rozšíření nezávislého dodavatele softwaru (ISV), protože sekundární displej nelze okamžitě konfigurovat a zobrazuje omezený obsah.

### <a name="payment-device"></a>Platební zařízení

Podpora platebního zařízení je implementována prostřednictvím platebního konektoru. Platební zařízení mohou provádět jednu nebo mnoho funkcí, které poskytují jiné třídy zařízení. Platební zařízení může například pracovat jako čtečka MSR/karet, řádkový displej, zařízení k odběru podpisů, nebo jako klávesnice na kódy PIN. Podpora pro platební zařízení je zavedena nezávisle na podpoře samostatných zařízení, která je k dispozici pro další zařízení, která jsou součástí hardwarového profilu.

## <a name="supported-interfaces"></a>Podporovaná rozhraní
### <a name="opos"></a>OPOS

Aby bylo možno zaručit, že spolu s aplikací Microsoft Dynamics 365 for Operations - Retail bude možné používat co nejširší škálu zařízení, je primární platformou pro maloobchodní periferní zařízení podporovanou aplikací Microsoft Dynamics 365 for Retail průmyslový standard OLE pro POS. Standard OLE pro POS byl vytvořen Národní maloobchodní federací (National Retail Federation, NRF), která stanovuje standardní komunikační protokoly pro maloobchodní periferní zařízení. OPOS je široce přijímaná implementace standardu OLE pro POS. Byla vyvinuta v polovině 90. let 20. století a od té doby několikrát aktualizována. OPOS poskytuje architekturu ovladačů zařízení, která umožňuje snadnou integraci hardwaru POS se systémy POS založenými na Windows. OPOS řídí zpracování komunikace mezi kompatibilním hardwarem a mezi softwarem POS. Ovládací prvek OPOS se skládá ze dvou částí:

-   **Objekt ovládacího prvku** – objekt ovládacího prvku pro určitou třídu zařízení (jako například řádkový displej) poskytuje rozhraní pro softwarový program. Konzultační služby Monroe (Monroe Consulting Services, [www.monroecs.com](http://www.monroecs.com/)) je společnost, která poskytuje standardizovanou sadu ovládacích prvků řízení OPOS, které jsou označovány jako objekty společných ovládacích prvků (Common Control Objects, CCO). CCO se používají k testování komponenty POS u Microsoft Dynamics 365 for Retail. Proto testování pomáhá zaručit, aby, pokud Microsoft Dynamics 365 for Retail podporuje nějakou třídu zařízení prostřednictvím OPOS, mohlo být podporováno mnoho typů zařízení za předpokladu, že výrobce dodává servisní objekt určený pro OPOS. Není nutné explicitně testovat každý typ zařízení.
-   **Objekt služby** – objekt služby zajišťuje komunikaci mezi objektem ovládacího prvku (CCO) a zařízením. Objekt služby pro nějaké zařízení obvykle pochází od výrobce zařízení. V některých případech však bude pravděpodobně nutné stáhnout objekt služby z webu výrobce. Například může být k dispozici novější objekt služby. Adresu webu výrobce najdete v dokumentaci k hardwaru.

[![Ovládací prvek objektu a objekt služby](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Podpora pro implementaci OPOS OLE pro POS pomáhá zaručit aby, v případě, že výrobci zařízení a vydavatelé POS standard správně implementují, mohly pokladní systémy a podporovaná zařízení řádně spolupracovat, i kdyby nebyly nejprve společně otestovány. **Poznámka:** Podpora OPOS nezaručuje podporu pro všechna zařízení, která mají ovladače OPOS. Microsoft Dynamics 365 for Retail musí nejprve podporovat tento typ zařízení nebo třídy prostřednictvím OPOS. Kromě toho objekty služby nemusí být vždy aktuální s nejnovější verzí CCO. Měli byste také pamatovat na to, že kvalita objektů služby bývá obecně různá.

### <a name="windows"></a>Windows

Tisk účtenky v POS je optimalizován pro OPOS. OPOS má tendenci být mnohem rychlejší než tisk pomocí systému Windows. Je tedy vhodné použít OPOS, zejména v maloobchodním prostředí, kde jsou tištěny účtenky se 40 sloupci a časy transakcí musí být rychlé. U většiny zařízení budete používat ovládací prvky OPOS. Některé tiskárny účtenek OPOS podporují také ovladače systému Windows. Pomocí ovladače pro Windows můžete získat přístup k nejnovějším písmům a jednu tiskárnu zařadit do sítě pro více pokladen. Použití ovladačů systému Windows má však také nevýhody. Následuje několik příkladů těchto nevýhod:

-   Při použití ovladačů Windows jsou obrázky před vytištěním vykreslovány. Tisk proto bývá pomalejší než u tiskáren, které používají ovládací prvky OPOS.
-   Zařízení, která jsou připojena prostřednictvím tiskárny („sériově“), nemusí při použití ovladače Windows správně fungovat. Například by se zásuvka s hotovostí nemusela otevřít nebo by tiskárna dokladů nemusela fungovat, jak má.
-   OPOS podporuje také rozsáhlejší sadu proměnných, které jsou specifické pro maloobchodní tiskárny účtenek, jako například řezání papíru nebo tisk účtenek.

Pokud budou pro tiskárnu systému Windows, kterou používáte, k dispozici ovládací prvky OPOS, tiskárna by měla s aplikací Microsoft Dynamics 365 for Retail stále pracovat správně.

### <a name="universal-windows-platform"></a>Univerzální platforma Windows

UWP se v případě maloobchodních periferních zařízení vztahuje na podporu systému Windows pro zařízení Plug and Play. Zařízení Plug and Play je připojeno k verzi operačního systému Windows, která tento typ zařízení podporuje. K použití zařízení dle způsobu určení není třeba žádný ovladač. Například pokud systém Windows rozpozná zařízení typu reproduktor Bluetooth, operační systém ví, že zařízení má typ třídy **reproduktor**. A bude s tímto zařízením nakládat jako s reproduktorem. Žádné další nastavení není třeba. V případě zařízení POS lze připojit mnoho zařízení USB a systém Windows je rozpozná jako zařízení standardu HID. Systém však nemusí být schopen určit schopnosti, které toto zařízení poskytuje, protože zařízení neurčuje třídu nebo typ zařízení. V systému Windows 10 byly přidány třídy zařízení pro čtečky čárových kódů a magnetických proužků. Proto pokud se zařízení systému Windows 10 ohlašuje jako zařízení jedné z těchto tříd, Windows bude ve vhodnou dobu naslouchat událostem ze zařízení. Modern POS podporuje UWP čtečky MSR a skenery. Proto když je připraven pro vstup z jednoho z těchto zařízení a bude připojeno zařízení patřící do jedné z těchto tříd, bude možno toto zařízení použít. Například pokud je k počítači s Windows 10 připojena čtečka čárových kódů UWP a je nakonfigurován vstup čárových kódů pro Modern POS, bude čtečka čárových kódů na přihlašovací obrazovce aktivní. Žádné další nastavení není třeba. Do systému Windows jsou přidávány další třídy zařízení UWP obslužných míst. Tyto třídy zahrnují třídy pro zásuvky s hotovostí a tiskárny účtenek. Podpora pro tyto nové třídy zařízení v Modern POS se očekává v brzké době.

### <a name="keyboard-wedge"></a>Převodník na signál klávesnice

Zařízení typu převodníku na signál klávesnice odesílá data do počítače, jako by tato data byla zadána na klávesnici. Proto ve výchozím nastavení obdrží pole, které je aktivní v POS, data z výsledku skenování nebo protahování proužku. V některých případech může toto chování způsobit načtení nesprávného typu dat do nesprávného pole. Například může být čárový kód naskenován do pole, které je určeno k zadání údajů platební karty. V mnoha případech je v POS logika, která určuje, zda data z výsledku skenování nebo protahování proužku jsou čárovým kódm nebo výsledkem protažení karty. Proto jsou pak data zpracována správně. Avšak jsou-li zařízení nastavena jako OPOS a ne jako zařízení typu převodníku na signál klávesnice, existuje větší možnost kontroly nad tím, jak budou data z těchto zařízení využívána, protože je více známo o zařízení, z nějž data pocházejí. Například data ze čtečky čárových kódů budou automaticky rozpoznána jako čárový kód a příslušný záznam v databázi bude nalezen mnohem snadněji a rychleji, než při použití obecného vyhledávacího řetězce, jako je tomu v případě zařízení typu převodníků na signál klávesnice.

### <a name="native-printer"></a>Nativní tiskárna

Nativní (neboli "Zařízení", jak je tento typ nazýván v hardwarovém profilu) tiskárny lze nakonfigurovat tak, aby zobrazily uživateli výzvu k výběru tiskárny nakonfigurované pro daný počítač. Jestliže je nakonfigurována tiskárna typu **Zařízení**, pak pokud Modern POS narazí příkaz pro tisk, bude uživatel vyzván k výběru tiskárny ze seznamu. Toto chování se liší od chování ovladačů pro systém Windows, protože typ tiskárny **Windows** v hardwarovém profilu nezobrazí seznam tiskáren. Namísto toho vyžadují, aby v poli **Název zařízení** byla uvedena pojmenovaná tiskárna.

### <a name="windows"></a>Windows

Typ zařízení **Windows** se používá pouze pro tiskárny. Když bude v hardwarovém profilu nakonfigurována tiskárna systému Windows, bude třeba zadat konkrétní název tiskárny. Když se Modern POS setká s tiskovou událostí, pak pokud je nakonfigurována tiskárna systému Windows, bude událost předána zadané tiskárně systému Windows. Uživatel nebude vyzván k výběru tiskárny.

### <a name="network"></a>Síť

Ze sítě adresovatelné zásuvky s hotovostí, tiskárny účtenek a platební terminály lze používat po síti buďto přímo prostřednictvím hardwarové stanice interprocesní komunikace (Interprocess Communications, IPC), která je integrována do aplikace Modern POS for Windows, nebo prostřednictvím hardwarové stanice služby IIS pro ostatní klienty Modern POS.

## <a name="hardware-station-deployment-options"></a>Možnosti nasazení hardwarové stanice
### <a name="ipc-built-in"></a>IPC (vestavěný)

Hardwarová stanice Interprocesní komunikace (Interprocess Communications, IPC) je součástí aplikace Modern POS for Windows. Chcete-li použít hardwarovou stanici IPC, přiřaďte k registru hardwarový profil, který bude používat aplikaci Modern POS for Windows. Pak vytvořte hardwarovou stanici typu **Vyhrazený** pro obchod, kde bude registr používán. Když spustíte Modern POS, bude hardwarová stanice IPC aktivní a periferie POS, které byly nakonfigurovány, budou připraveny k použití. Jestliže z nějakého důvodu dočasně nepožadujete místní hardware, použijte operaci **Spravovat hardwarové stanice** k vypnutí schopností hardwarové stanice. Modern POS může také využívat hardwarovou stanici IPC k přímé komunikaci se síťovými periferními zařízeními.

### <a name="iis"></a>služba IIS,

Službu IIS nebo samostatnou verzi hardwarové stanice můžete využívat dvěma způsoby. Deskriptor "IIS" znamená, že aplikace POS se k hardwarové stanici připojuje prostřednictvím Internetové informační služby Microsoft. Aplikace POS se k hardwarové stanici služby IIS připojuje prostřednictvím webových služeb, které jsou spuštěny v počítači, ke kterému jsou zařízení připojena. Při použití služby IIS může kterákoli registrační pokladna POS nacházející se na stejné síti jako hardwarová stanice IIS využívat maloobchodní periferní zařízení připojená k hardwarové stanici. Protože pouze Modern POS for Windows obsahuje integrovanou podporu pro maloobchodní periferní zařízení, všechny ostatní aplikace Modern POS musejí používat hardwarovou stanici služby IIS ke komunikaci s periferiemi POS, které jsou nakonfigurovány v hardwarovém profilu. Proto každá instance služby hardwarové stanice IIS vyžaduje počítač, na kterém je spuštěna webová služba a aplikaci, která komunikuje s zařízeními. Hardwarová stanice IIS je nezbytná pro všechny aplikace Modern POS, které nejsou pro Windows.

#### <a name="dedicated"></a>Vyhrazeno

Moderní POS používá hardwarové stanice **Vyhrazeného** typu ke zjišťování, zda jsou periferní zařízení přímo připojena k počítači, na kterém je aplikace používána. Avšak typ **Vyhrazený** lze používat také pro hardwarové stanice služby IIS. V tradičním pevném scénáři POS, který používá Cloud POS jako aplikaci Retail POS, se typ hardwarové stanice **Vyhrazený** používá pro hardwarové stanice služby IIS, které jsou nasazeny ve stejném počítači, na kterém je spuštěn Cloud POS. Z hlediska maloobchodních periferní zařízení, vyhrazené hardwarové stanice IIS mají větší podporu periferních zařízení pro tradiční pevné scénáře POS. Vyhrazené hardwarové stanice podporují všechna periferní zařízení, která jsou podporována v hardwarovém profilu.

#### <a name="shared"></a>Sdílený

Sdílené hardwarové stanice jsou určeny pro použití více zařízeními POS v průběhu dne. Sdílené hardwarové stanice jsou optimalizovány tak, že podporují pouze zásuvky s hotovostí, tiskárny účtenek a platební terminály. Nelze přímo připojit samostatné čtečky čárových kódů, MSR, řádkové displeje, váhy či jiná zařízení. Jinak bude docházet ke konfliktům, když se více zařízení POS pokusí nárokovat si tato periferní zařízení současně. Zde je způsob správy konfliktů u podporovaných zařízení:

-   **Zásuvka s hotovostí** – Zásuvka se otevírá prostřednictvím události, která se odesílá do zařízení. Jediný problém, ke kterému může docházet při volání zásuvky s hotovostí, nastává tehdy, když je zásuvka s hotovostí již otevřena. V případě sdílených hardwarových stanic by měla být zásuvka s hotovostí v hardwarovém profilu nastavena na **Sdílené**. Toto nastavení zabrání POS v kontrole, zda je zásuvka již otevřena při odesílání příkazů k otevření.
-   **Tiskárna účtenek** – Budou-li do hardwarové stanice odeslány dva příkazy pro tisk účtenek současně, může se jeden z příkazů můžete ztratit, což závisí na zařízení. Některá zařízení mají interní paměť nebo sjednocené prostředky, které mohou tomuto problému zabránit. Pokud tiskový příkaz není úspěšný, pokladník obdrží chybovou zprávu a můžete tiskový příkaz zopakovat z programu POS.
-   **Platební terminál** – Jestliže se pokladník pokusí zařídit transakci na platebním terminálu, který je již používán, bude pokladník upozorněn zprávou, že terminál je používán, a požádán, aby se o tuto akci pokusil později. Pokladníci obvykle sami zjistí, že terminál je již používán, a než se znovu pokusí o řízení, počkají na dokončení druhé transakce.

Pro budoucí verze je plánováno ověřování za účelem detekce, zda jsou nepodporovaná zařízení nakonfigurována pro hardwarový profil mapovaný na sdílenou hardwarovou stanici. Pokud budou zjištěna jakákoli nepodporovaná zařízení, uživatel obdrží zprávu uvádějící, že zařízení nejsou pro sdílené hardware stanice podporována. V případě sdílených hardwarových stanic je volba **Vybrat po řízení** nastavena na **Ano** na úrovni registru. Uživatel POS je potom vyzván k výběru hardwarové stanice při výběru nabídky pro transakci v POS. Vybráno hardwarové stanice pouze v době vyhlášení výběr hardware stanice přidá přímo do pracovního postupu POS pro mobilní scénáře. Další výhodou je, že zobrazený řádek na platebním terminálu není použit pro sdílené scénáře. Pokud je platební terminál použit pro zobrazení řádku, ostatní uživatelé mohou být blokováni od používání tohoto terminálu, dokud transakce neskončí. V mobilních scénářích mohou být přidány řádky ke transakci za delší období. Proto možnost **Vybrat při úhradách** je vyžadována k zajištění optimální dostupnosti zařízení.

### <a name="network-peripherals"></a>Síťová příslušenství

Označení sítí pro zařízení v profilu hardwaru umožňuje připojit zásuvky na hotovosti, tiskárny účtů a platební terminály prostřednictvím síťového připojení.

#### <a name="modern-pos-for-windows"></a>Moderní POS pro Windows

Můžete určit adresy IP síťových příslušenství na dvou místech. Pokud Moderní POS klient systému Windows používá jednu sadu síťových příslušenství, měli byste nastavit adresy IP těchto zařízení pomocí možnosti **konfigurace IP** v Podokně akcí u samotné registrační pokladny. V případě síťových zařízení, která budou sdílena mezi registry POS, může být hardwarový profil, který má přidělena síťová zařízení, mapován přímo na sdílenou hardwarovou stanici. Chcete-li přiřadit adresy IP, vyberte tuto hardwarovou stanici na stránce **Maloobchodní obchody**, potom použijte volbu **Konfigurace IP** v sekci **Hardwarové stanice** pro zadání síťových zařízení, která budou přiřazena k této hardwarové stanici. U hardwarových stanic, které mají pouze síťová zařízení, nemusíte instalovat samotnou hardwarovou stanici. V tomto případě je hardwarová stanice požadována pouze za účelem konceptuálního seskupení síťově adresovatelných zařízení podle jejich umístění v maloobchodě.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Cloudový POS, Moderní POS pro iOS a Moderní POS pro Android

Logika, která řídí fyzicky připojené a síťově adresovatelné periferie, je obsažena v hardwarové stanici. Proto pro všechny klienty POS kromě Moderního POS pro Windows musí být zavedena a aktivní hardwarová stanice IIS umožňující těmto POS komunikovat s periferními zařízeními bez ohledu na to, zda jsou tyto periferie fyzicky připojeny k hardwarové stanici nebo adresovány po síti.

## <a name="setup-and-configuration"></a>Instalace a konfigurace
### <a name="hardware-station-installation"></a>Instalace hardwarové stanice

Informace naleznete v tématu [Konfigurace a instalace maloobchodní hardwarové stanice](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Instalace a konfigurace Moderního POS pro Windows

Informace naleznete v tématu [Konfigurace a instalace maloobchodního Moderního POS](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>Instalace a konfigurace zařízení OPOS

Další informace o součástech OPOS naleznete v části "Podporovaná rozhraní" v tomto dokumentu. Ovladače OPOS obvykle poskytuje výrobce zařízení. Když je nainstalován ovladač zařízení OPOS, přidá se klíč registru systému Windows do jednoho z následujících umístění:

-   **32bitový systém:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64bitový systém:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

V rámci umístění registru ServiceOPOS jsou nakonfigurovaná zařízení uspořádána podle třídy zařízení OPOS. Více ovladačů zařízení je uloženo.

## <a name="supported-scenarios-by-hardware-station-type"></a>Podporované scénáře podle typu hardwaru stanice
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Podpora klientů – IPC hardwarová stanice vs. IIS hardwarová stanice

V následující tabulce jsou uvedeny podporované topologie a scénáře nasazení.

| Klient      | Hardwarová stanice IPC | Hardwarová stanice IIS |
|-------------|----------------------|----------------------|
| Aplikace systému Windows | Ano                  | Ano                  |
| Cloud POS   | Žádný                   | Ano                  |
| Android     | Žádný                   | Ano                  |
| iOS         | Žádný                   | Ano                  |

### <a name="network-peripherals"></a>Síťová příslušenství

Periferní síťová zařízení mohou být podporována přímo prostřednictvím hardwarové stanice, jež je integrována do aplikace Moderního POS pro Windows. Pro ostatní klienty je nutné nasadit hardwarovou stanici IIS.

| Klient      | Hardwarová stanice IPC | Hardwarová stanice IIS |
|-------------|----------------------|----------------------|
| Aplikace systému Windows | Ano                  | Ano                  |
| Cloud POS   | Žádný                   | Ano                  |
| Android     | Žádný                   | Ano                  |
| iOS         | Žádný                   | Ano                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Podporované druhy zařízení podle typu hardwaru stanice
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderní POS pro systém Windows s hardwarovou stanicí IPC (vestavěnou)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Podporovaná třída zařízení</th>
<th>Podporovaná rozhraní</th>
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
<li>UWP (Není nutná instalace.)</li>
<li>Převodník na signál klávesnice (Není nutná instalace.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Výstavce</td>
<td><ul>
<li>OPOS</li>
<li>Síťová <strong>poznámka:</strong> pouze jednu zásuvku lze nastavit v případě, pokud je nastaveno na zásuvce <strong>Použití sdílené směny</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zásuvka 2</td>
<td><ul>
<li>OPOS</li>
<li>Síťová <strong>poznámka:</strong> pouze jednu zásuvku lze nastavit v případě, pokud je nastaveno na zásuvce <strong>Použití sdílené směny</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skener</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Není nutná instalace.)</li>
<li>Převodník na signál klávesnice (Není nutná instalace.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skener 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Není nutná instalace.)</li>
<li>Převodník na signál klávesnice (Není nutná instalace.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Měřítko</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Klávesnice pro kód PIN</td>
<td>OPOS (podpora je poskytována prostřednictvím přizpůsobení platebního konektoru.)</td>
</tr>
<tr class="even">
<td>Zaznamenání podpisu</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Patební terminál </td>
<td><ul>
<li>Podpora vlastního zařízení</li>
<li>Síť (další informace naleznete v dokumentaci konektoru platby.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Všechny moderní POS klienty, které mají vyhrazené hardwarové stanice IIS

**Poznámka:** pokud je hardwarová stanice "vyhrazena", je vztah 1:1 mezi klientem POS a hardwarovou stanicí.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Podporovaná třída zařízení</th>
<th>Podporovaná rozhraní</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tiskárna</td>
<td><ul>
<li>OPOS</li>
<li><strong>Poznámka</strong> k ovladači Windows: U tiskáren Windows v síti musí mít uživatel hardwarové stanice oprávnění k přístupu k tiskárně.</li>
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
<li>Síťová <strong>poznámka:</strong> pouze jednu zásuvku na každý hardwarový profil lze nastavit v případě, pokud je nastaveno na zásuvce <strong>Použití sdílené směny</strong>.</li>
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
<td>OPOS (podpora je poskytována prostřednictvím přizpůsobení platebního konektoru.)</td>
</tr>
<tr class="odd">
<td>Podpis zachycení</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Patební terminál </td>
<td><ul>
<li>Podpora vlastního zařízení</li>
<li>Síť (další informace naleznete v dokumentaci konektoru platby.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Všechny moderní POS klienty, které mají sdílenou hardwarovou stanici IIS

**Poznámka:** Když je hardwarová stanice IIS "sdílena", více zařízení může používat hardwarovou stanici najednou. V tomto scénáři byste měli používat pouze zařízení uvedená v následující tabulce. Pokud se pokoušíte sdílet zařízení, která zde nejsou uvedena, jako například čtečky čárových kódů a MSR, dojde k chybě, jakmile se několik zařízení pokusí uplatnit stejné periferní zařízení. V budoucnu se takové konfiguraci explicitně zabrání.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Podporovaná třída zařízení</th>
<th>Podporovaná rozhraní</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tiskárna</td>
<td><ul>
<li>OPOS</li>
<li><strong>Poznámka</strong> k ovladači Windows: U tiskáren Windows v síti musí mít uživatel hardwarové stanice oprávnění k přístupu k tiskárně.</li>
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
<li>Síťová <strong>poznámka:</strong> pouze jednu zásuvku na každý hardwarový profil lze nastavit v případě, pokud je nastaveno na zásuvce <strong>Použití sdílené směny</strong>.</li>
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
<li>Síť (další informace naleznete v dokumentaci konektoru platby.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Konfigurace pro podporované scénáře
Další informace o vytváření hardwarových profilů naleznete v tématu [Definování a udržování kanálových klientů, včetně registrů a hardwarových stanic](define-maintain-channel-clients-registers-hw-stations.md). **Poznámka:** V aplikaci Microsoft Dynamics 365 for Retail, verze 1611 se hardwarový profil stanice již nepoužívá. Atributy, které jste dříve nastavili v profilu hardwarové stanice, jsou nyní součástí samotné hardwarové stanice.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Moderní POS pro systém Windows s hardwarovou stanicí IPC (vestavěnou)

Tato konfigurace je nejtypičtější konfigurací tradičních pevných POS registrů. Pro tento scénář jsou informace o hardwarovém profilu mapovány přímo do samotného registru. Číslo terminálu EFT by mělo být také nastaveno v samotném registru. Chcete-li nastavit tuto konfiguraci, postupujte následujícím způsobem:

1.  Vytvořte profil hardwaru, ve kterém jsou nakonfigurovány všechny potřebné periferie.
2.  Namapovat hardwarový profil k pokladně POS.
3.  Pak vytvořte hardwarovou stanici typu **Vyhrazený** pro obchod, kde bude pokladna POS používána. Popis je volitelný. **Poznámka:** Na hardwarové stanici nemusíte nastavovat žádné jiné vlastnosti. Všechny další požadované informace, například profil hardwaru budou pocházet ze samotné poklady.
4.  Klikněte na **Maloobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
5.  Vyberte plán distribuce **1090** pro synchronizování nového hardwarového profilu do úložiště. Klikněte na tlačítko **Nyní spustit** pro synchronizování změn do POS.
6.  Vyberte plán distribuce **1040** pro synchronizování nové hardwarové stanice do úložiště. Klikněte na tlačítko **Nyní spustit** pro synchronizování změn do POS.
7.  Instalace a aktivace moderní POS pro systém Windows.
8.  Spusťte moderní POS pro systém Windows spustit a začněte používat připojená periferní zařízení.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Všechny moderní POS klienty, které mají vyhrazené hardwarové stanice IIS

Tato konfigurace může být použita pro všechny moderní POS klienty, které mají hardwarovou stanici, která je používána výlučně jednou pokladnou POS. Chcete-li nastavit tuto konfiguraci, postupujte následujícím způsobem:

1.  Vytvořte profil hardwaru, ve kterém jsou nakonfigurovány všechny potřebné periferie.
2.  Pak vytvořte hardwarovou stanici typu **Vyhrazený** pro obchod, kde bude pokladna POS používána.
3.  Na vyhrazené hardwarové stanici nastavte následující vlastnosti:
    -   **Název hostitele** – název hostitelského počítače kde bude spuštěna hardwarová stanice. **Poznámka:** Cloudová POS dokáže rozluštit **localhost** pro určení místního počítače, kde běží tato cloudová POS. Certifikát, který je požadován pro spárování cloudové POS s hardwarovou stanicí, však musí mít jako název počítače také "Localhost". Chcete-li se vyhnout problémům, doporučujeme v případě potřeby uvést instanci každé vyhrazené hardwarové stanice pro úložiště. Pro každou hardwarovou stanici by měl název hostitele odpovídat názvu počítače, kde bude tato hardwarová stanice umístěna.
    -   **Port** – Port, který má hardwarová stanice použít pro komunikaci s moderním POS klientem.
    -   **Hardwarový profil** - Není-li hardwarový profil poskytován na samotné hardwarové stanici, použije se hardwarový profil, který je přiřazen k pokladně.
    -   **Číslo EFT POS** – ID terminálu EFT, které je použito při odesílání EFT autorizací. Toto ID je poskytováno procesorem platební karty.
    -   **Název balíčku** – balíček hardwarové stanice pro použití při nasazení hardwarové stanice.

4.  Klikněte na **Maloobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
5.  Vyberte plán distribuce **1090** pro synchronizování nového hardwarového profilu do úložiště. Klikněte na tlačítko **Nyní spustit** pro synchronizování změn do POS.
6.  Vyberte plán distribuce **1040** pro synchronizování nové hardwarové stanice do úložiště. Klikněte na tlačítko **Nyní spustit** pro synchronizování změn do POS.
7.  Instalace hardwarové stanice. Další informace o instalaci hardwarové stanice, viz [Konfigurace a instalace maloobchodní hardwarové stanice](retail-hardware-station-configuration-installation.md).
8.  Instalace a aktivace moderní POS. Další informace o instalaci moderní POS, viz [Instalace a konfigurace moderní POS pro maloobchod](retail-modern-pos-device-activation.md).
9.  Přihlášte se do moderní POS a vyberte **Provést operace bez zásuvky**.
10. Spusťte operaci **Spravovat hardwarové stanice**.
11. Klikněte na **Spravovat**.
12. Na stránce správy hardwarových stanic použijte možnost zapnutí hardwarové stanice.
13. Vyberte hardwarovou stanici, kterou chcete použít a potom klikněte na **Spárovat**.
14. Poté, co je hardwarová stanice spárována, klikněte na tlačítko **Zavřít**.
15. Na stránce výběru hardwarové stanice klikněte na nedávno vybranou hardwarovou stanici, abyste ji aktivovali.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Všechny moderní POS klienty, které mají sdílenou hardwarovou stanici IIS

Tato konfigurace může být použita pro všechny moderní POS klienty, které sdílejí hardwarové stanice s jinými zařízeními. Chcete-li nastavit tuto konfiguraci, postupujte následujícím způsobem:

1.  Vytvořte hardwarový profil, ve kterém jsou nakonfigurovány potřebné periferie.
2.  Pak vytvořte hardwarovou stanici typu **Sdílený** pro obchod, kde bude pokladna POS používána.
3.  Na sdílené hardwarové stanici nastavte následující vlastnosti:
    -   **Název hostitele** – název hostitelského počítače kde bude spuštěna hardwarová stanice.
    -   **Popis** – Text, který pomůže identifikovat hardwarovou stanici, jako například **Vratky** nebo **Přední část obchodu**.
    -   **Port** – Port, který má hardwarová stanice použít pro komunikaci s moderním POS klientem.
    -   **Hardwarový profil** – každá sdílená hardwarové stanice by měla mít svůj hardwarový profil. Hardwarové profily lze sdílet mezi jednotlivými hardwarovými stanicemi, ale musí být namapovány na každou z nich. Navíc doporučujeme použít sdílené směny, pokud více zařízení používá stejnou sdílenou hardwarovou stanici. Pro nastavení sdílené směny, klikněte na **Maloobchodní prodej** &gt; **Konfigurace kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Hardwarové profily**. Pro každý sdílený hardwarový profil vyberte zásuvku hotovosti a nastavte možnost **Zásuvka sdílené směny** na **Ano**.
    -   **Číslo EFT POS** – ID terminálu EFT, které je použito při odesílání EFT autorizací. Toto ID je poskytováno procesorem platební karty.
    -   **Název balíčku** – balíček hardwarové stanice pro použití při nasazení hardwarové stanice.

4.  Opakujte kroky 2 a 3 pro každou další hardwarovou stanici, která je v obchodě vyžadována.
5.  Klikněte na **Maloobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
6.  Vyberte plán distribuce **1090** pro synchronizování nového hardwarového profilu do úložiště. Klikněte na tlačítko **Nyní spustit** pro synchronizování změn do POS.
7.  Vyberte plán distribuce **1040** pro synchronizování nové hardwarové stanice do úložiště. Klikněte na tlačítko **Nyní spustit** pro synchronizování změn do POS.
8.  Nainstalujte hardwarovou stanici na každý hostitelský počítač, který jste vytvořili v krocích 2 a 3. Další informace o instalaci hardwarové stanice, viz [Konfigurace a instalace maloobchodní hardwarové stanice](retail-hardware-station-configuration-installation.md).
9.  Instalace a aktivace moderní POS. Další informace o instalaci moderní POS, viz [Instalace a konfigurace moderní POS pro maloobchod](retail-modern-pos-device-activation.md).
10. Přihlášte se do moderní POS a vyberte **Provést operace bez zásuvky**.
11. Spusťte operaci **Spravovat hardwarové stanice**.

12. Klikněte na **Spravovat**.
13. Na stránce správy hardwarových stanic použijte možnost zapnutí hardwarové stanice.
14. Vyberte hardwarovou stanici, kterou chcete použít a potom klikněte na **Spárovat**.
15. Zopakujte krok 14 pro každou hardwarovou stanici, kterou bude používat moderní POS.
16. Jakmile jsou spárovány všechny potřebné hardwarové stanice, klikněte na tlačítko **Zavřít**.
17. Na stránce výběru hardwarové stanice klikněte na nedávno vybranou hardwarovou stanici, abyste ji aktivovali. **Poznámka:** Pokud zařízení často používají různé hardwarové stanice, doporučujeme, abyste nakonfigurovali moderní POS tak, aby vyzvaly pokladníky k výběru hardwarové stanice při zahájení úhradového procesu. Klikněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Pokladny**. Vyberte pokladu a poté nastavte možnost **Vybrat při úhradě** na **Ano**. Použijte plán distribuce **1090** k synchronizování změn do databáze kanálů.

## <a name="extensibility"></a>Rozšiřitelnost
Pro více informací o scénářích rozšiřitelnosti hardwarových stanic, viz [Rozšíření hardwarových stanic](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Zabezpečení
Podle stávajících bezpečnostních standardů je třeba ve výrobním prostředí použít následující nastavení: **Poznámka:** Instalátor hardwarových stanic automaticky provede tyto úpravy registru jako součást instalace prostřednictvím samoobsluhy.

-   Protokol Secure Sockets Layer (SSL) by měl být vypnut.
-   Je třeba povolit a používat pouze bezpečnostní vrstvu Transport Layer Security (TLS) verze 1.2 (nebo stávající nejnovější verzi). **Poznámka:** Ve výchozím nastavení, SSL a všechny verze TLS, s vyjímkou TLS 1.2, jsou zakázány. Chcete-li upravit nebo povolit tyto hodnoty, postupujte takto:
    1.  Stiskněte klávesu s logem Windows + R pro otevření okna **Spustit**.
    2.  V poli **Otevřít** zadejte **Regedit** a potom klikněte na tlačítko **OK**.
    3.  Pokud se zobrazí okno **Řízení uživatelských účtů**, klikněte na tlačítko **Ano**.
    4.  V okně **Editoru registru** přejděte na **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Následující klíče byly automaticky vloženy, aby umožnily použití pouze protokolu TLS 1.2:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Žádné další síťové porty by neměly být otevřené, pokud nejsou vyžadovány ze známých a konkrétních důvodů.
-   Sdílení prostředků mezi zdroji musí být zakázáno a musí specifikovat povolené zdroje, které jsou akceptovány.
-   K získání certifikátů, které budou použity v počítačích, které spouštějí hardwarovou stanici, by měly být použity pouze důvěryhodné certifikační autority.

**Poznámka:** Je velmi důležité, abyste přezkoumali bezpečnostní pokyny IIS a také požadavky od Payment Card Industry (PCI).

## <a name="peripheral-simulator"></a>Simulátor periferních zařízení
Informace naleznete v tématu [Maloobchodní simulátor periferií](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Periferní zařízení otestována Microsoftem
### <a name="ipc-built-in-hardware-station"></a>Hardwarová stanice IPC (vestavěná)

Následující periferní zařízení byla testována pomocí hardwarové stanice IPC, která je zabudována do moderního POS pro systém Windows.

#### <a name="printer"></a>Tiskárna

| Výrobce | Model    | Rozhraní | Poznámky                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Vlastní    | Připojeno prostřednictvím sítě   |
| Star         | mPOP     | OPOS      | Připojeno pomocí Bluetooth |
| HP           | F7M67AA  | OPOS      | Napájené USB             |

#### <a name="bar-code-scanner"></a>Skener čárových kódů

| Výrobce  | Model         | Rozhraní | Poznámky |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Symbol        | LS2208        | OPOS      |          |
| HP Integrated | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>Klávesnice pro kód PIN

| Výrobce | Model  | Rozhraní | Poznámky                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Vyžaduje úpravu konektoru platby |

#### <a name="payment-terminal"></a>Patební terminál 

| Výrobce | Model | Rozhraní | Poznámky                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Vlastní    | Vyžaduje úpravu konektoru platby                                |
| VeriFone     | MX925 | Vlastní    | Vyžaduje úpravu konektoru platby; připojeno prostřednictvím sítě a USB |
| VeriFone     | MX915 | Vlastní    | Vyžaduje úpravu konektoru platby; připojeno prostřednictvím sítě a USB |

#### <a name="cash-drawer"></a>Zásuvka s hotovostí

| Výrobce | Model     | Rozhraní | Poznámky                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Připojeno pomocí Bluetooth |
| APG          | Atwood    | Vlastní    | Připojeno prostřednictvím sítě   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Řádkový displej

| Výrobce  | Model   | Rozhraní | Poznámky |
|---------------|---------|-----------|----------|
| HP Integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

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

### <a name="dedicated-iis-hardware-station"></a>Vyhrazená hardwarová stanice IIS

Následující periferní zařízení byly testovány pomocí vyhrazené, nesdílené, hardwarové stanice (IIS), společně s moderním POS pro systém Windows a cloudovým POS.

#### <a name="printer"></a>Tiskárna

| Výrobce | Model    | Rozhraní | Poznámky                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Vlastní    | Připojeno prostřednictvím sítě     |
| Star         | TSP100   | OPOS      | Vyžaduje ovladače TSP650II |
| HP           | F7M67AA  | OPOS      | Napájené USB               |

#### <a name="bar-code-scanner"></a>Skener čárových kódů

| Výrobce  | Model   | Rozhraní | Poznámky |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Symbol        | LS2208  | OPOS      |          |
| HP Integrated | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>Klávesnice pro kód PIN

| Výrobce | Model  | Rozhraní | Poznámky                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Vyžaduje úpravu konektoru platby |

#### <a name="payment-terminal"></a>Patební terminál 

| Výrobce | Model | Rozhraní | Poznámky                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Vlastní    | Vyžaduje úpravu konektoru platby                                |
| VeriFone     | MX925 | Vlastní    | Vyžaduje úpravu konektoru platby; připojeno prostřednictvím sítě a USB |
| VeriFone     | MX915 | Vlastní    | Vyžaduje úpravu konektoru platby; připojeno prostřednictvím sítě a USB |

#### <a name="cash-drawer"></a>Zásuvka s hotovostí

| Výrobce | Model     | Rozhraní | Poznámky              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Vlastní    | Připojeno prostřednictvím sítě |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Řádkový displej

| Výrobce  | Model   | Rozhraní | Poznámky |
|---------------|---------|-----------|----------|
| HP Integrated | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

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

### <a name="shared-iis-hardware-station"></a>Sdílená hardwarová stanice IIS

Následující periferní zařízení byla testována pomocí sdílené hardwarové stanice (IIS), společně s moderním POS pro systém Windows a cloudovým POS. **Poznámka:** je podporována pouze tiskárna, platební terminál a zásuvka hotovosti.

#### <a name="printer"></a>Tiskárna

| Výrobce | Model    | Rozhraní | Poznámky                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Vlastní    | Připojeno prostřednictvím sítě     |
| Star         | TSP100   | OPOS      | Vyžaduje ovladače TSP650II |
| HP           | F7M67AA  | OPOS      | Napájené USB               |

#### <a name="payment-terminal"></a>Patební terminál 

| Výrobce | Model | Rozhraní | Poznámky                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Vlastní    | Vyžaduje úpravu konektoru platby; připojeno prostřednictvím sítě a USB |
| VeriFone     | MX915 | Vlastní    | Vyžaduje úpravu konektoru platby; připojeno prostřednictvím sítě a USB |

#### <a name="cash-drawer"></a>Zásuvka s hotovostí

| Výrobce | Model     | Rozhraní | Poznámky              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Vlastní    | Připojeno prostřednictvím sítě |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Řešení potíží
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Moderní POS může detekovat hardwarové stanice v seznamu pro výběr, ale nemůže dokončit spárování

**Řešení:** zkontrolujte následující seznam možných bodů selhání:

-   Počítač, na kterém běží moderní POS, důvěřuje certifikátu používanému v počítači, který spouští hardwarovou stanici.
    -   Chcete-li ověřit tato nastavení, přejděte na následující adresu URL ve webovém prohlížeči: https://&lt;Název počítače&gt;:&lt;Číslo portu&gt;/HardwarováStanice/ping.
    -   Tato adresa URL použije příkaz ping k ověření, zda je počítač dostupný a prohlížeč ukáže, zda je certifikát důvěryhodný. (Například v aplikaci Internet Explorer se zobrazí ikona zámku v adresním řádku. Po kliknutí na tuto ikonu Internet Explorer ověří, zda je certifikát v současné době důvěryhodný. Můžete nainstalovat certifikát na místní počítač pomocí zobrazení podrobností o aktuálně zobrazeném certifikátu.)
-   V počítači, který spouští hardwarovou stanici, je v bráně firewall otevřen port, který tato hardwarová stanice používá.
-   Hardwarová stanice správně nainstalovala informace o obchodním účtu pomocí nástroje Instalovat informace o obchodníkovi, který běží na konci instalátoru hardwarové stanice.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Moderní POS nemůže rozpoznat hardwarovou stanici v seznamu pro výběr

**Řešení:** tento problém může způsobit některý z následujících faktorů:

-   Hardwarová stanice nebyla v sídle správně nastavena. Pomocí kroků uvedených dříve v tomto tématu ověřte, zda je správně zadán profil hardwarové stanice a hardwarová stanice.
-   Úlohy nebyly spuštěny pro aktualizaci konfigurace kanálu. V takovém případě spusťte úlohu 1070 pro konfiguraci kanálu.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Moderní POS neodráží nové nastavení pokladní zásuvky

**Řešení:** Uzavřete aktuální dávku. Změny v zásuvce s hotovostí nejsou načteny do moderního POS, dokud není aktuální dávka uzavřena.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Moderní POS hlásí problém s maloobchodní periferií

**Řešení:** Zde jsou některé obvyklé příčiny tohoto problému:

-   Ujistěte se, že další nástroje pro konfiguraci ovladače zařízení jsou uzavřeny. Pokud tyto nástroje jsou otevřeny, mohou zabránit modernímu POS nebo hardwarové stanici ve vyžádání zařízení.
-   Pokud je maloobchodní periferie sdílena s více zařízeními POS, ujistěte se, že patří k jedné z následujících kategorií:
    -   Zásuvka s hotovostí
    -   Tiskárna účtenek
    -   Patební terminál 

    Pokud periferie nepatří do jedné z těchto kategorií, není hardwarová stanice navržena tak, aby umožňovala sdílení periferií mezi více POS zařízeními.
-   Někdy mohou ovladače zařízení způsobit, že běžné ovládací objekty (CCO) přestanou správně fungovat. Pokud bylo zařízení nedávno nainstalováno a nyní nepracuje správně nebo si všimnete jiných problémů, lze často vyřešit tento problém přeinstalací CCO. Pro stažení CCO běžte na stránku <http://monroecs.com/oposccos_current.htm>.
-   Pokud provádíte časté změny periferních zařízení během testování nebo odstraňování problémů, pravděpodobně budete muset obnovit službu IIS namísto čekání na obnovení samotné mezipaměti. Chcete-li provést reset služby IIS, postupujte takto:
    1.  V nabídce **Start** napište **CMD**.
    2.  V okně Výsledky hledání klikněte pravým tlačítkem myši na **Příkazový řádek** a potom klikněte na tlačítko **Spustit jako správce**.
    3.  V okně **Příkazový řádek** napište příkaz **iisreset /Restart** a stiskněte klávesu Enter.
    4.  Po restartu IIS restartujte také moderní POS.
-   Během častých změn periferních zařízení, pokud často spouštíte a opoušíte klient POS, může proces dllhost z předchozí relace POS zasahovat do aktuální relace. V tomto případě zařízení nemusí být použitelné, dokud nezavřete hostitele knihovny dynamické vazby (DLL), která spravuje předchozí relaci. Chcete-li zavřít hostitele DLL, postupujte takto:
    1.  V nabídce **Start** napište **Správce úloh**.
    2.  V okně Výsledky hledání klikněte na tlačítko **Správce úloh**.
    3.  Ve Správci úloh na kartě **Podrobnosti** klikněte na záhlaví sloupce, který je označen jako **Jméno** pro seřazení tabulky abecedně.
    4.  Skrolujte níže, dokud nenajdete dllhost.exe.
    5.  Vyberte každou DLL hostitele a potom klikněte na tlačítko **Ukončit úlohu**.
    6.  Jakmile byli hostitelé DLL uzavřeni, restartujte také moderní POS.


<a name="see-also"></a>Viz také
--------

[Periferní simulátor pro maloobchod](dev-itpro/retail-peripheral-simulator.md)




