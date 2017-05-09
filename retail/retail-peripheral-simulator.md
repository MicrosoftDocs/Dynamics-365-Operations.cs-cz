---
title: "Periferní simulátor pro maloobchod"
description: "Toto téma popisuje nástroj pro periferní simulaci, který je součástí Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 42dc414ff2bb6359b47d89c3bd3c510e4258f816
ms.openlocfilehash: b2229466040351d8c2b9494b30b4c928651820b8
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripheral-simulator"></a>Periferní simulátor pro maloobchod

[!include[banner](includes/banner.md)]


Toto téma popisuje nástroj pro periferní simulaci, který je součástí Microsoft Dynamics 365 for Operations - Retail.

<a name="overview"></a>Přehled
--------

Periferní simulátor pro Microsoft Dynamics 365 for Operations - Retail je nástroj, který pomáhá nastavit, testovat a řešit potíže s periferními zařízeními, která se používají v maloobchodním prostředí. Tento simulátor můžete používat pro usnadnění testování periferních zařízení v maloobchodě a k izolaci problémů způsobených nesprávně nastavených nebo chybně fungujících ovladačů zařízení. Simulátor zahrnuje program pro stolní počítače, který nabízí virtuální verze zařízení, která Dynamics 365 for Operations - Retail podporuje. Oddíl pro každé virtuální zařízení zobrazuje interakce mezi zařízením a maloobchodním pokladním místem (POS). Můžete ho také použít k zadáním vstupu, který je platný pro různé scénáře POS. Periferní simulátor podporuje interakci mezi POS a následujícími virtuálními zařízeními:

-   **Tiskárna** – periferní simulátor může zobrazit příjemky, které jsou nakonfigurovány pro tiskárnu POS.
-   **Řádek zobrazení** – můžete nakonfigurovat virtuální displej linky, který zobrazuje aktivitu na displeji fyzické linky.
-   **Čtečka magnetického proužku (MSR)** – Do POS můžete odesílat simulované události magnetického proužku z periferního simulátoru.
-   **Zásuvka** – můžete simulovat fyzickou zásuvku na pokladní hotovost.
-   **Zásuvka 2** – nastavením druhé zásuvky na hotovost v periferním simulátoru můžete simulovat scénáře zahrnující jeden registr POS, který je aktivní pro dvě směny.
-   **Skener** – virtuální skener čárových kódů, který podporuje periferní simulátor, může vystavovat události skenování čárového kódu.
-   **Váha** – virtuální váha umožňuje simulovat interakci vážených položky s POS.
-   **Klávesnice pro osobní identifikační číslo (PIN)** – můžete simulovat operace klávesnice pro zadání PIN. **Poznámka:** Musíte implementovat podporu pro fyzickou klávesnici pro kód PIN prostřednictvím konektoru platby.
-   **Zaznamenání podpisu** – periferní simulátor zahrnuje zařízení pro záznam virtuálního podpisu, které lze nastavit na zobrazení výzvy pro podpisy, které jsou požadovány pro některé nabídky, například platby z účtu zákazníka.

Periferní simulátor můžete použít také pro simulaci události platebního terminálu klávesnice, které pocházejí z čtečky čárového kódu a MSR. Virtuální periferní simulátor konkrétně podporuje propojování a vkládání objektů pro zařízení Retail POS (OPOS).

## <a name="key-scenarios"></a>Základní scénáře
### <a name="troubleshooting"></a>Řešení potíží

Periferní simulátor můžete použít k odstraňování problémů s instalací zařízení. Pokud nemáte periferní simulátor nebo druhé zařízení stejného druhu, může být obtížné určit, odkud problémy pocházejí. Pokud však máte periferní simulátor, můžete nastavit virtuální zařízení a spustit stejné cesty kódu cesty a obchodní logiky, které se používají pro fyzické zařízení. Z pohledu periferního simulátoru spočívá hlavní rozdíl mezi virtuálními a fyzickými zařízeními v objektu služby nebo ovladači zařízení. Pro fyzická zařízení poskytuje objekt služby výrobce zařízení. Naopak pro periferní simulátor jsou objekty služby poskytovány jako součást periferního simulátoru. Když periferní simulátor pracuje správně a zařízení nepracuje správně po změně názvu zařízení v hardwarovém profilu na název skutečného zařízení, lze předpokládat, že je problém s objektem služby poskytnutém výrobcem.

### <a name="training"></a>Školení

Periferní simulátor můžete použít k přidání realistické vrstvy ke školení pokladníka, když není k dispozici nastavení fyzického hardwaru. Když je periferní simulátor součástí scénářů školení, může pokladník efektivněji pracovat s POS poskytnutím vstupu, jako jsou skeny kódu produktu čárového kódu a projetí dárkové karty, a sledováním, které příjemky se pro konkrétní transakci vytisknou.

### <a name="testing"></a>Testování

Periferní simulátor můžete použít k testování čárových kódů, formátů účtenek a podobně, aniž byste museli instalovat fyzický hardware ve virtuálním prostředí. Protože není požadován fyzický hardware a nemusíte nasazovat klienta POS do hardware stanice nebo fyzického počítače, můžete rychleji otestovat změny provedené v účetním systému.

## <a name="set-up-the-peripheral-simulator"></a>Nastavení periferního simulátoru
### <a name="set-up-a-hardware-profile"></a>Nastavení profilu hardwaru

1.  Při nastavování periferního simulátoru přejděte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Profily hardwaru**.
2.  Pokud chcete vytvořit nový profil, klikněte na **Nový**.
3.  Zadejte hodnoty do polí **Číslo profilu** a **Popis**.
4.  Chcete-li nastavit virtuální zařízení, která musí být testována, použijte následující tabulku. V tomto poli jsou vysvětleny sloupce v tabulce:
    -   **Zařízení** – tento sloupec obsahuje název pevné záložky, kterou rozbalíte pro nastavení zařízení.
    -   **Typ zařízení** – tento sloupec obsahuje hodnotu, kterou jste vybrali v poli označeném názvem zařízení.
    -   **Název zařízení** – tento sloupec udává přesnou hodnotu, kterou zadáte pro název zařízení. **Důležité:** názvy zařízení, které jsou zde uvedeny jsou požadovány, protože hardwarová stanice používá tyto konkrétní názvy k adresování zařízení. Pokud nepoužíváte tyto konkrétní názvy, nebude možné zařízení použít.

    | Zařízení            | Typ zařízení | Název zařízení              |
    |-------------------|-------------|--------------------------|
    | Tiskárna           | OPOS        | MockOPOSPrinter          |
    | Řádkový displej      | OPOS        | MockOPOSLineDisplay      |
    | MSR               | OPOS        | MockOPOSMSR              |
    | Výstavce            | OPOS        | MockOPOSDrawer1          |
    | Drawer2           | OPOS        | MockOPOSDrawers          |
    | Skener           | OPOS        | MockOPOSScanner          |
    | Měřítko             | OPOS        | MockOPOSScale            |
    | klávesnice pro kód PIN           | OPOS        | MockOPOSPinPad           |
    | Zaznamenání podpisu | OPOS        | MockOPOSSignatureCapture |

**Poznámka:** Žádné zvláštní nastavení v profilu hardwaru není požadováno pro simulaci akcí klávesnice ze skeneru čárového kódu a MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Přiřazení profilu hardwaru k pokladně

1.  Po vytvoření hardwarového profilu přejděte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Registry**.
2.  V seznamu **Registry POS** klikněte na odkaz v poli **Číslo registru** pro registr, který by měl použít periferní simulátor.
3.  Klikněte na možnost **Upravit**.
4.  V části **Profily** v poli **Hardwarový profil** vyberte hardwarový profil, který jste vytvořili pro virtuální příslušenství.
5.  Klikněte na možnost **Uložit**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synchronizace změn do databáze kanálu

1.  Přejděte do nabídky **Maloobchodní a velkoobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
2.  Vyberte plán distribuce **1090**.
3.  Klepněte na tlačítko **Spustit**, chcete-li synchronizovat změny v POS.

Po synchronizaci dat jsou k dispozici nový profil hardwaru a změny v registru v databázi kanálu.

## <a name="install-the-peripheral-simulator"></a>Instalace periferního simulátoru
1.  Přejděte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Hardwarové profily**.
2.  Klepněte na tlačítko **Stáhnout**a potom klepněte na **PeripheralSimulator**. **Poznámka:** Musíte vypnout blokování automaticky otevíraných oken před stažením periferního simulátoru.
3.  Po dokončení stahování otevřete složku **Stažené soubory** složky a poklepejte na **VirtualPeripherals.msi** ke spuštění instalačního programu.
4.  Nainstalujte periferní simulátor pomocí výchozího nastavení.

Kromě periferního simulátoru je třeba nainstalovat objekty společných ovládacích prvků ze služby Monroe Consulting Services. V opačném případě nebude periferní simulátor pracovat správně. Chcete-li stáhnout objekty společných ovládacích prvků, přejděte na <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Použití periferního simulátoru
Periferní simulátor spustíte kliknutím na **Start** v počítači, zadejte **Maloobchodní periferní simulátor** a pak vyberte aplikaci, když se objeví ve výsledcích hledání. Po spuštění periferního simulátoru klikněte na název zařízení k zobrazení podporovaných zařízení. Tato zařízení se zobrazí jako karty na levé straně okna. Chcete-li zobrazit určité zařízení, klepněte na kartu pro dané zařízení.

### <a name="line-display-capabilities"></a>Možnosti řádkového displeje

Zobrazení řádku je první zařízení, které je uvedeno jako periferní simulátor. Když je nakonfigurován displej virtuálního řádku, ukazuje položky řádky, jak jsou naskenovány v transakci POS. Vedle položek řádku se zobrazuje součet, který je splatný při výběru výběrového řízení v POS. Také se ukazuje, splatný zůstatek v případě, že je nabídka je zadána, ale zůstatek je pro transakci stále splatný. Pokud POS není používán, může se zobrazit zpráva, že je že uzavřena pokladna. Zprávu musíte nakonfigurovat na kartě **Zobrazení řádku** v profilu hardwaru.

### <a name="cash-drawer-capabilities"></a>Schopnosti zásuvky s hotovostí

Zobrazení zásuvky s hotovostí je druhé zařízení, které je uvedeno jako periferní simulátor. Pokud je hardwarový profil konfigurován pro použití virtuální zásuvky, POS Otevře zásuvku pro aktivní směnu v reakci na operace zásuvky, jako jsou výkazy výběrových řízení a pokladník tak může změnit nebo vložit hotovost během standardní transakce cash-and-carry. Virtuální zásuvky mají popisky **hlavní zásuvka** a **sekundární zásuvka**. Tyto popisky představují zásuvku a zásuvku 2 v hardwarovém profilu. Při zavření zásuvky se zobrazí obrázek zavřené zásuvky a tlačítko na zavřené zásuvce hotovostí je označeno **Otevřít zásuvku**. Pokud klepnete na toto tlačítko, obrázek bude nahrazen obrázkem otevřené zásuvky. Tlačítko na otevřené zásuvce je označeno **zavřít zásuvku**. Několik operací v POS může způsobit otevření zásuvky. Většina operací nemůže pokračovat, když je zásuvka otevřená. Výjimkou jsou některé postupy na konci dne. Pokud uživatel POS uživatel obdrží chybovou zprávu, která uvádí že operaci nelze provést, při otevřené zásuvce, musí uživatel zavřít virtuální nebo fyzickou zásuvku a pokračovat. Pokud je pokladní zásuvka označena jako **sdílené** v hardwarovém profilu, systém neověří, že zásuvka je zavřená před operaci. Operace pokračuje obvyklým způsobem, i když je zásuvka otevřená. Toto chování podporuje scénáře kde zásuvky jsou sdíleny mezi prodejci a když jeden zaměstnanec použije zásuvku, druhý provádí úlohy nesouvisející s jeho vlastním zařízením POS. Změny provedené v zásuvce nejsou zřejmé, dokud aktuální směna není uzavřena a není otevřena nová směna.

### <a name="msr-capabilities"></a>Schopnosti MSR

Periferní simulátor poskytuje rozsáhlou podporu pro virtuální operace MSR při práci v režimu OPOS nebo režimu platebního terminálu klávesnice. Režim OPOS vyžaduje, aby oddíl MSR byl nakonfigurován v hardwarovém profilu, aby pracoval jako zařízení OPOS. Režim platebního terminálu klávesnice odešle pouze události dat platebního terminálu klávesnice do systému Microsoft Windows. Kromě rozdílů v nastavení se OPOS a režim platebního terminálu klávesnice liší následujícími způsoby:

-   Klient POS umožňuje zařízení OPOS MSR pro konkrétní scénáře, jako jsou scénáře, které povolují data magnetického proužku věrnostní nebo položku dárkové karty.
-   V režimu platebního terminálu klávesnice odešle periferní simulátor data platebního terminálu klávesnice do pole, které je aktivní, pokud jsou data odeslána. Toto chování se podobá chování, které nastane, když se data zadávají pomocí klávesnice. Pokud chcete použít oddíl MSR jako platební terminál klávesnice, musí uživatel přepnout na Retail Modern POS (MPOS) a ujistit se, že jsou přijímána data ve správném poli. Proto můžete nakonfigurovat zpoždění, tak aby uživatel měl čas zajistit, že data budou odeslána do správného pole.

#### <a name="testing-gift-and-payment-card-swipes"></a>Testování proužků dárkových a platebních karet

Virtuální oddíl MSR, který poskytuje periferní simulátor, také umožňuje nakonfigurovat určitá data na scénáře testování proužků dárkových a platebních karet. Chcete-li vytvořit kartu, klepněte na znaménko plus (**+**) a vyberte typ karty. Potom zadejte číslo karty nebo dat sledování, která mají být odeslána do POS spolu s měsícem a rokem vypršení platnosti karty, kterou definujete. Hodnota, kterou jste vybrali v poli **Typ karty** je pouze popisek, který lze mapovat na kartu pole. Tento štítek usnadňuje identifikaci karet, když jsou protažené přes periferní simulátor. Můžete vybrat karty, které byly nakonfigurovány v periferním simulátoru pomocí tlačítek šipka vlevo (**&lt;**) a šipka vpravo (**&gt;**) nad obrazem na kartě tlačítka. Můžete upravit a odstranit karty pomocí tlačítek **Upravit** a **Odstranit** tlačítka vedle znaménka plus (**+**).

### <a name="pin-pad"></a>Klávesnice pro kód PIN

Můžete nakonfigurovat simulátor klávesnice pro zadávání PIN pro simulaci klávesnice OPOS PIN. Když se transakce s prostředky elektronického přenosu (EFT) provádí v POS a vyžaduje zadání PIN, hardwarová stanice volá zařízení k zobrazení výzvy k zadání PIN kódu. Aby klávesnice pro kód PIN fungovala, vyžaduje periferní simulátor podporu konektor platby EFT.

### <a name="printer"></a>Tiskárna

Virtuální periferní tiskárna zobrazuje příjmy tak, jak budou vytištěny v POS. Pokud operace tisku vytváří více příjemek, můžete je procházet.

#### <a name="configure-receipt-printing"></a>Konfigurace tisku příjemek

1.  Přejděte na **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Hardwarové profily**.
2.  Vyberte hardwarový profil, který jste vytvořili virtuální periferní zařízení.
3.  Na pevné záložce **Tiskárna** klikněte na **Upravit**.
4.  V poli **ID profilu příjemky** vyberte profil příjemky.
5.  Klikněte na možnost **Uložit**.

### <a name="scale"></a>Měřítko

Při přidání produktu na váze k transakci POS a když je váha nakonfigurována, POS načte hmotnost z rozsahu. Pro virtuální a fyzickou váhu by měl být produkt nebo hmotnosti stanoven před přidáním produktu do transakce. Před přidáním produktu na váze do transakce přejděte na váhu v periferním simulátoru a použijte tlačítka (**+**) a mínus (**–**) k nastavení hmotnosti, kterou by váha měla vykázat. Můžete také zadat přímo v požadované hmotnosti do pole **Aktuální hodnota**. Jednotky hmotnosti pro váhu můžete nastavit pomocí tlačítek plus (**+**), **Upravit** a **Odstranit**. Tímto způsobem lze určit jednotky založené na produktech, které jsou váženy nebo na národním prostředí, kde se váha používá.

#### <a name="configure-a-scale-product"></a>Konfigurace váhy

1.  Přejděte do nabídky **Maloobchod a** **obchod** &gt; **Produkty a kategorie** &gt; **Uvolnit produkty podle kategorie**.
2.  Otevřete záznam produktu.
3.  Vyberte produkt ke zvážení.
4.  Na pevné záložce **Maloobchod** nastavte možnost **Zvážit produkt** z **Ne** na **Ano**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synchronizace změn do databáze kanálu

1.  Přejděte do nabídky **Maloobchodní a velkoobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
2.  Vyberte plán distribuce **1040**.
3.  Klepněte na tlačítko **Spustit**, chcete-li synchronizovat změny v POS.

Po synchronizaci dat a přidání váženého produktu do transakce POS zkontroluje POS váhu.

### <a name="signature-capture"></a>Zaznamenání podpisu

Zařízení pro záznam virtuálních podpisů výzve uživatele k zadání podpisu na klávesnici pro záznam virtuálních podpisů, kdy použitá nabídka vyžaduje podpis. Uživatel může přijmout podpis k zobrazení v POS. Pokladník může pak přijmout podpis. Podpis je pak uložen spolu s nabídkou a je synchronizován zpět do účetního systému společně s dalšími daty transakce.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Nastavení nabídky na vyžadování podpisu

1.  Přejděte do nabídky **Maloobchodní a velkoobchodní prodej** &gt; **Kanály** &gt; **Maloobchodys** &gt; **Všechny maloobchody**.
2.  Vyberte maloobchod.
3.  Klikněte na možnost **Upravit**.
4.  Klikněte na **Nastavit** a v části **Nastavit** klikněte na **Metody platby**.
5.  Klikněte na možnost **Upravit**.
6.  Vyberte způsob platby, který vyžaduje podpis.
7.  V části **Obecné** pod **Zachycení podpisu** nastavte **Použít digitalizační zařízení pro podpis** na **Ano**.
8.  V poli **Minimální částka pro zachycení podpisu** zadejte minimální částku, která by měla vyvolat zaznamenání podpisu.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synchronizace změn do databáze kanálu

1.  Přejděte do nabídky **Maloobchodní a velkoobchodní prodej** &gt; **Maloobchodní IT** &gt; **Distribuční plán**.
2.  Vyberte plán distribuce **1070**.
3.  Klepněte na tlačítko **Spustit**, chcete-li synchronizovat změny v POS.

Pokud po synchronizaci dat použitá nabídka vyžaduje podpis a částka splňuje prahovou hodnotu podpisu, zobrazí POS výzvu k zadání podpisu na zařízení pro záznam virtuálního podpisu.

## <a name="additional-configuration"></a>Další konfigurace
Můžete upravit konfigurační soubor periferního simulátoru, aby lépe řešil testované scénáře. Konfigurační soubor najdete zde C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurační soubor definuje jednotky, které jsou k dispozici pro testování na váze, typy karet, které jsou k dispozici pro testování a typy čárového kódu. Úpravou textové hodnoty v konfiguračním souboru můžete například přidat nový typ karty nebo měrnou jednotku, kterou lze vybrat za běhu. Nové hodnoty se zobrazí po restartování aplikace.

## <a name="troubleshooting"></a>Řešení potíží
Aktivity pro periferní simulátor jsou zaznamenány v periferním simulátoru. Protokol najdete zde C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Periferní simulátor také hlásí problémy do protokolu událostí systému Windows, který je dostupný zde: **Protokoly aplikací a služeb** &gt; **Microsoft** &gt; **DynamicsAX**. Pokud změny provedené v profilu hardwaru nebo jiných oblastech nejsou zřejmé, při použití MPOS nebo periferního simulátoru zkontrolujte distribuční úlohy plánovače, které používá k synchronizaci dat s databází kanálu. Pokud byly synchronizovány změny, ale nejsou patrné v POS, restartujte klienta POS. Změny nakonfigurovaných zásuvek hotovosti nebudou účinné, dokud nevytvoříte novou směnu. Proto pokud provedete změny zásuvky, vždy uzavřete stávající směnu, abyste otestovali nové nastavení pokladní zásuvky. Někdy může ovladač způsobit, že společné objekty kontroly přestanou správně fungovat. Děje se tak, pokud je ovladač od výrobce nainstalován po společných řídicích objektech ze služby Monroe Consulting Services. V takovém případě přeinstalujte objekty společných ovládacích prvků.

<a name="see-also"></a>Viz také
--------

[Přehled maloobchodních periferních zařízení](retail-peripherals-overview.md)




