---
title: "Maloobchodní periferní simulátor"
description: "Toto téma popisuje periferní simulátor nástroj, který je součástí Microsoft Dynamics 365 pro operace - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
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

# <a name="retail-peripheral-simulator"></a>Maloobchodní periferní simulátor

[!include[banner](includes/banner.md)]


Toto téma popisuje periferní simulátor nástroj, který je součástí Microsoft Dynamics 365 pro operace - Retail.

<a name="overview"></a>Přehled
--------

365 Microsoft Dynamics pro operace - maloobchodní periferní simulátor je nástroj, který pomáhá vytvořit, testovat a Poradce při potížích s periferními zařízeními, které se používají v prostředí maloobchodu. Periferní simulátor můžete zjednodušit testování maloobchodní periferní zařízení a izolovat problémy, které jsou způsobeny nesprávnou instalací nebo nefunkční ovladače zařízení. Stolní program, který nabízí virtuální verze zařízení že 365 Dynamics pro operace zahrnuje periferní simulátor - maloobchod podporuje. Oddíl pro každý virtuální počítač zobrazuje interakce mezi zařízením a maloobchodní místa prodeje (POS). Lze je také použít poskytovat vstup, který je platný pro různé scénáře POS. Simulátor periferní podporuje interakci mezi POS a následující virtuální zařízení:

-   **Tiskárny** – periferní simulátor můžete zobrazit příjmy, které jsou nakonfigurovány pro tiskárnu POS.
-   **Řádek zobrazení** – můžete nakonfigurovat virtuální Řádkový displej na fyzické řádku zobrazení zobrazit aktivity.
-   **Čtečka magnetického proužku (MSR)** – POS můžete odeslat události simulované magnetického proužku z periferní simulátor.
-   **Zásobník na** – můžete simulovat fyzikální hotovostí.
-   **Zásobník 2** – nastavením druhou zásuvku v periferní simulátor můžete simulovat scénáře zahrnující jeden Pokladna POS, který byl aktivní na dvě směny.
-   **Skener** – virtuální čárový kód skener, který podporuje periferní simulátor mohou vystavovat události skenování čárového kódu.
-   **Měřítko** – virtuální měřítko umožňuje simulovat působení zvážené položky POS.
-   **Osobní identifikační číslo (PIN) pad** – můžete simulovat PIN pad operací. **Poznámka:** musí implementovat podporu pro fyzické klávesnice pro kód PIN do konektoru platby.
-   **Zaznamenání podpisu** – periferní simulátor zahrnuje zařízení pro digitalizaci virtuální podpis, který lze nastavit na zobrazení výzvy pro podpisy, které jsou požadovány pro některé nabídky, například platby s účtem zákazníka.

Periferní simulátor můžete použít také pro simulaci klávesnice wedge události, které pocházejí z čtečka čárového kódu a MSR. Virtuální simulátor periferní konkrétně podporuje propojování a vkládání objektů pro Retail POS (OPOS) zařízení.

## <a name="key-scenarios"></a>Klíčové scénáře
### <a name="troubleshooting"></a>Řešení potíží

Periferní simulátor slouží k odstraňování problémů při instalaci zařízení. Pokud nemáte periferní simulátor nebo druhé zařízení stejného druhu, může být obtížné určit, kde problémy pocházejí. Však pokud máte periferní simulátor, můžete nastavit virtuální zařízení a spustit stejný kód cesty a obchodní logiky, které se používají pro fyzické zařízení. Hlavní rozdíl mezi virtuální a fyzické zařízení z hlediska periferní simulátor je objekt služby nebo ovladače zařízení. Fyzické zařízení, pro objekt služby poskytované výrobcem zařízení. Naopak periferní simulátor objekty služby jsou poskytovány jako součást periferní simulátor. Při periferní simulátor pracuje správně, pokud zařízení nepracuje správně, po změně názvu zařízení v hardwarovém profilu název skutečné zařízení, lze předpokládat, že je problém s objekt služby poskytované výrobcem.

### <a name="training"></a>Školení

Periferní simulátor lze přidat realistické vrstvu na pokladníka, vzdělávání, když není k dispozici nastavení fyzického hardwaru. Při periferní simulátor je součástí přípravy scénáře, pokladník efektivněji pracovat s POS poskytnutím vstup například produkt bar kód kontroly a dárkové karty swipes a pozorováním příjmy jsou vytištěny pro určitou transakci.

### <a name="testing"></a>Testování

Periferní simulátor můžete vyzkoušet produkt čárových kódů, formáty účtenek a podobně, aniž by museli instalovat fyzický hardware ve virtuálním prostředí. Změny provedené v back office můžete otestovat rychleji, protože fyzický hardware není nutné a nemusíte nasazení POS klienta na hardware stanice nebo fyzického počítače.

## <a name="set-up-the-peripheral-simulator"></a>Nastavení periferních simulátor
### <a name="set-up-a-hardware-profile"></a>Nastavení profilů hardwaru

1.  Periferní simulátor nastavení, přejděte na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily**.
2.  Chcete-li vytvořit nový profil, klepněte na **nové**.
3.  Zadejte hodnoty do **číslo profilu** a **popis** pole.
4.  Chcete-li nastavit virtuální zařízení, které musí být testovány pomocí následující tabulky. Zde je vysvětlení sloupců v tabulce:
    -   **Zařízení** – tento sloupec obsahuje název záložku s náhledem, rozbalte nastavení zařízení.
    -   **Typ zařízení** – tento sloupec obsahuje hodnotu, kterou jste vybrali v poli, který je označen název zařízení.
    -   **Název zařízení** – tento sloupec udává přesnou hodnotu, kterou zadáte pro název zařízení. **Důležité:** názvy zařízení, které jsou zde uvedeny jsou požadovány, protože hardware stanice používá tyto konkrétní názvy zařízení řeší. Pokud nepoužíváte tyto konkrétní názvy, nebude možné zařízení použít.

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

**Poznámka:** žádné zvláštní nastavení v profilu hardwaru je požadováno pro simulaci klávesnice wedge události ze skeneru čárového kódu a MSR.

### <a name="assign-the-hardware-profile-to-a-register"></a>Přiřazení profilu hardwaru k rejstříku

1.  Po vytvoření hardwarového profilu, přejděte na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**registruje**.
2.  V **Registry POS** seznam, klepněte na odkaz v **číslo žurnálu** pole pro registr, který by měl použít periferní simulátor.
3.  Klikněte na možnost **Upravit**.
4.  V **profily** oddílu **hardwarový profil** vyberte hardwarový profil, který jste vytvořili virtuální příslušenství.
5.  Click **Save**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synchronizovat změny databáze kanálu

1.  Přejít na **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**.
2.  Vyberte **1090** plán distribuce.
3.  Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny v POS.

Po synchronizaci dat jsou k dispozici v databázi kanálu nového hardwarového profilu a změny v registru.

## <a name="install-the-peripheral-simulator"></a>Instalace periferních simulátor
1.  Přejít na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily**.
2.  Klepněte na tlačítko **Stáhnout**a potom klepněte na **PeripheralSimulator**. **Poznámka:**, musíte vypnout blokování automaticky otevíraných před stažením periferní simulátor.
3.  Po dokončení stahování otevřete **stažení** složky a poklepejte na **VirtualPeripherals.msi** Chcete-li spustit instalační program.
4.  Instalace periferních simulátor s použitím výchozího nastavení.

Kromě okrajových simulátor je třeba nainstalovat objekty společných ovládacích prvků z Monroe konzultaci služby. V opačném případě se periferní simulátor nebudou pracovat správně. Chcete-li stáhnout objekty společných ovládacích prvků, přejděte na <http://monroecs.com/oposccos_current.htm>.

## <a name="using-the-peripheral-simulator"></a>Pomocí simulátoru periferní
Periferní simulátor spustíte klepnutím na **spuštění** v počítači, zadejte **maloobchodní periferní simulátor**a když se objeví ve výsledcích hledání vyberte aplikace. Po spuštění simulátoru periferní klepnutím na název zařízení, viz podporované zařízení. Tato zařízení se zobrazí jako karty na levé straně okna. Chcete-li zobrazit určité zařízení, klepněte na kartu pro dané zařízení.

### <a name="line-display-capabilities"></a>Možnosti zobrazení řádku

Zobrazení řádku je první zařízení, které je uvedeno v periferní simulátor. Při konfiguraci virtuální Řádkový displej zobrazuje řádek položky jako jsou prohledány v POS transakcí. Vedle položky řádku jsou zobrazeny celkem, která je splatná při výběru nabídky v POS. Také ukazuje, splatné saldo pokud nabídka je zadána, ale zůstatek je stále splatnosti transakce. Pokud POS není používán, může být zobrazeno zprávu označíte, že uzavření pokladny. Zprávy, musíte nakonfigurovat na **řádek zobrazení** s náhledem v hardwarovém profilu.

### <a name="cash-drawer-capabilities"></a>Funkce pokladní zásuvky

Zásuvku je druhé uvedené v simulátoru periferní zařízení. Pokud hardwarový profil konfigurován pro použití virtuální zásuvky, POS Otevře zásuvku pro aktivní posun v reakci na zásuvku operace, jako jsou výkazy úhrad a tak, aby Pokladník může změnit nebo vkladu hotovosti během standardní cash-and-carry transakcí. Virtuální zásuvky mají popisky **hlavní zásuvky** a **sekundární zásobník**. Tyto popisky představují zásuvky a zásuvku 2 v hardwarovém profilu. Při zavření šuplíku obrázku uzavřené hotovostí a tlačítko na uzavřené hotovostí je označen **otevřít zásuvku**. Pokud klepnete na toto tlačítko obrázek nahrazen obraz otevřít zásuvku zásuvky je nyní otevřít. Tlačítko na Otevřít zásuvku je označen **zavřít zásuvku**. Chcete-li otevřít zásuvku může způsobit několik operací v POS. Většina operací nemůže pokračovat v otevřeném hotovostí. Výjimkou jsou některé postupy koncový den. Pokud POS uživatel obdrží chybovou zprávu, která uvádí operaci nelze provést, při otevřeném zásuvku, musí uživatel zavřete virtuální nebo fyzický zásuvku pokračovat. Pokud pokladní zásuvku je označena jako **sdílené** v hardwarovém profilu, systém nedokazuje, že zásuvky je uzavřena před operaci. Operace pokračuje obvyklým způsobem, i když je otevřít zásuvku. Toto chování podporuje scénáře kde zásuvky jsou sdíleny prodejcům a jedno spojení používá hotovostí, zatímco jiné přidružit provádí úlohy nesouvisející na vlastní zařízení POS. Změny provedené na zásuvku nejsou zřejmé, dokud aktuální směny je uzavřen a otevření nové směny.

### <a name="msr-capabilities"></a>MSR schopnosti

Periferní simulátor poskytuje rozsáhlou podporu pro virtuální operace MSR při práci v režimu OPOS nebo režimu klávesnice wedge. OPOS režimu vyžaduje, aby oddíl MSR konfiguraci v hardwarovém profilu pracovat jako zařízení OPOS. Režimu klávesnice wedge odešle pouze klávesnice wedge dat událostí systému Windows. Kromě rozdílů v nastavení OPOS a klávesnice wedge režimy liší následujícími způsoby:

-   Klient POS umožňuje zařízení OPOS MSR pro konkrétní scénáře, jako jsou scénáře, které umožňují dat magnetického proužku věrnostní nebo položku dárkové karty.
-   V režimu klávesnice wedge odešle periferní simulátor klávesnice wedge data pole je aktivní, pokud jsou data odeslána. Toto chování se podobá chování, který nastane, pokud se data zadaná pomocí klávesnice. Pokud chcete použít oddíl MSR jako klávesnice wedge, musí uživatel přepnout na maloobchodní moderní POS (MPOS) a ujistěte se, že jsou přijímána data ve správném poli. Zpoždění, proto můžete nakonfigurovat tak, aby uživatel nemá čas a ujistěte se, že údaje budou odeslány na správné pole.

#### <a name="testing-gift-and-payment-card-swipes"></a>Swipes testování dárek a platební karty

Virtuální oddíl MSR, který poskytuje periferní simulátor také umožňuje nakonfigurovat určitá data MSR otestovat scénáře swipes dárek a platební karty. Chcete-li vytvořit kartu, klepněte na znaménko plus (**+**) tlačítko a vyberte typ karty. Potom zadejte číslo karty nebo sledování dat, který má být odeslán do POS a vypršení platnosti měsíc a rok pro karty, které definujete. Hodnota, kterou jste vybrali v **typu karty** je pouze popisek, který lze mapovat na kartu pole. Štítek je snazší identifikaci karty, pokud jejich jsou protažené přes periferní simulátor. Můžete vybrat karty, které byly nakonfigurovány v periferní simulátor pomocí šipka vlevo (**&lt;**) a pravou šipkou (**&gt;**) nad obrazem na kartě tlačítka. Můžete upravit a odstranit pomocí karty **úprava** a **odstranit** tlačítka vedle na znaménko plus (**+**) tlačítko.

### <a name="pin-pad"></a>Klávesnice pro kód PIN

Můžete nakonfigurovat simulátor PIN pad pro simulaci OPOS PIN pad. Při transakci prostředky elektronického přenosu (EFT) se provádí v POS a vyžaduje zadání PIN, hardware stanice volá výzvu k zadání PIN kódu PIN zařízení. Práce, klávesnice pro kód PIN periferní simulátoru vyžaduje podporu konektor platby EFT.

### <a name="printer"></a>Tiskárna

Virtuální tiskárnu periferní právě zobrazuje příjmy budou vytištěny v POS. Pokud operaci tisku vytváří více příjemek, můžete procházet příjmy.

#### <a name="configure-receipt-printing"></a>Nastavit tisk účtenky

1.  Přejít na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily**.
2.  Vyberte hardwarový profil, který jste vytvořili virtuální příslušenství.
3.  Na **tiskárna** s náhledem, klikněte na tlačítko **upravit**.
4.  V **ID profilu účtenky** vyberte profil účtenky.
5.  Click **Save**.

### <a name="scale"></a>Měřítko

Když produkt měřítka je přidána k transakci POS a měřítkem je nakonfigurován, POS hmotnost zkopíruje z rozsahu. Pro oba virtuální a fyzické měřítko produktu nebo hmotnosti stanovit před přidáním produktu do transakce. Před přidáním produktu měřítko k transakci, přejděte na stupnici periferní simulátoru a použít znaménko plus (**+**) a mínus (**–**) tlačítek, které vykazují stupnice hmotnosti. Můžete také zadat přímo v požadované hmotnosti **aktuální hodnotu** pole. Jednotky hmotnosti pro měřítko můžete nastavit pomocí znaménka plus (**+**), **úprava**, a **odstranit** tlačítka. Tímto způsobem lze určit jednotky založené na produkty, které se zváží nebo národní prostředí, kde se používá stupnice.

#### <a name="configure-a-scale-product"></a>Konfigurace produktu stupnice

1.  Přejít na **maloobchodní a****commerce**&gt;**produkty a kategorie**&gt;**uvolněných produktů podle kategorie**.
2.  Otevřete záznam produktu.
3.  Vyberte produkt pro vážení.
4.  Na **Retail** s náhledem nastavení **měřítku produkt** možnost z **č** k **Ano**.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synchronizovat změny databáze kanálu

1.  Přejít na **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**.
2.  Vyberte **1040** plán distribuce.
3.  Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny v POS.

Po synchronizaci dat, při přidání produktu stupnice transakce POS, POS zkontroluje stupnice pro hmotnost.

### <a name="signature-capture"></a>Zaznamenání podpisu

Zařízení pro digitalizaci virtuální podpis výzvu zajistit podpis na panelu pro zachycení virtuální podpis podpis vyžaduje nabídku, která se používá. Uživatel může přijímat podpisu zobrazíte v POS. Pokladník může pak přijmout podpis. Podpis je pak uložena spolu s nabídky a je synchronizována zpět úřadu společně s dalšími údaji transakce.

#### <a name="set-up-a-tender-to-require-a-signature"></a>Nastavení nabídky vyžadovat podpis

1.  Přejít na **maloobchodní a commerce**&gt;**kanály**&gt;**maloobchodní obchody**&gt;**všechny maloobchodní obchody**.
2.  Vyberte k maloobchodu.
3.  Klikněte na možnost **Upravit**.
4.  Klepněte na tlačítko **nastavit**a pak **nastavit** klepněte na **metody platby**.
5.  Klikněte na možnost **Upravit**.
6.  Vyberte způsob platby, který vyžaduje podpis.
7.  V **Obecné** v sekci **zachycení podpisu**, nastavte **použít podpis digitalizační zařízení** možnost na **Ano**.
8.  V **minimální částka pro zachycení podpisu** zadejte minimální částku, kterou by mělo dojít k zaznamenání podpisu.

#### <a name="synchronize-changes-to-the-channel-database"></a>Synchronizovat změny databáze kanálu

1.  Přejít na **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**.
2.  Vyberte **1070** plán distribuce.
3.  Klepněte na tlačítko **nyní spustit** Chcete-li synchronizovat změny v POS.

Po synchronizaci dat vyžadující podpis slouží nabídka a částka splňuje práh podpis, POS vyzve k podpisu na podpis virtuální zařízení pro digitalizaci.

## <a name="additional-configuration"></a>Další konfigurace
Můžete upravit periferní simulátor konfigurační soubor, aby lépe řešení situací, které při testování. Můžete najít konfigurační soubor c:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Konfigurační soubor definuje jednotky, které jsou k dispozici pro testování na stupnici, typy karet, které jsou k dispozici pro testování a typy čárového kódu. Úpravou textové hodnoty v konfiguračním souboru můžete například přidat nový typ karty nebo měrnou jednotku, kterou lze vybrat za běhu. Nové hodnoty se zobrazí po restartování aplikace.

## <a name="troubleshooting"></a>Řešení potíží
Aktivity pro periferní simulátoru jsou zaznamenány v periferní simulátor. Do protokolu můžete najít na C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. Periferní simulátor také hlásí problémy do protokolu událostí systému Windows, které je dostupné na **aplikace a služby protokoly**&gt;**Microsoft**&gt;**aplikace Dynamics AX**. Pokud změny provedené v profilu hardwaru nebo jiných oblastí nejsou zřejmé, při použití MPOS nebo periferní simulátor, zkontrolujte distribuční úlohy plánovače, které používá k synchronizaci dat s databází kanálu. Pokud byly synchronizovány změny, ale nejsou patrné v POS, restartujte klienta POS. Nakonfigurované zásuvky změny nebudou účinné, dokud je vytvořen nový shift. Proto pokud provedete změny do zásuvky, přesvědčte se, zda vždy zavřít stávající shift, chcete-li otestovat nastavení nové pokladní zásuvky. V některých případech po běžné ovládací prvek objekty ze služby Monroe Consulting Services je nainstalován ovladač od výrobce, ovladač může způsobit běžné objekty řízení přestal správně fungovat. V takovém případě nainstalujte objekty společných ovládacích prvků.

<a name="see-also"></a>Viz také
--------

[Retail peripherals overview](retail-peripherals-overview.md)




