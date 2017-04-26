---
title: "Definovat a spravovat klienty kanálu, registry a hardware stanice"
description: "Tato wiki popisuje postup připojení periferních zařízení k vaší pokladně POS."
author: josaw1
manager: AnnBe
ms.date: 2016-06-15 20 - 49 - 33
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dee5745670ad86000795f2913f99f49c0f123a00
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Definovat a spravovat klienty kanálu, registry a hardware stanice

Tato wiki popisuje postup připojení periferních zařízení k vaší pokladně POS.

**Poznámka:** konkrétní pokyny k instalaci naleznete v tématu [Konfigurace a instalace hardwarové stanice pro maloobchod](retail-hardware-station-configuration-installation.md) a [Samoobslužné stažení/instalace řešení Retail Modern POS a aktivace zařízení Modern POS a Cloud POS](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Klíčové komponenty
Několik komponent slouží k definování vztahů mezi úložištěm, pokladním místem (POS) nebo kanálů v rámci obchodu a maloobchodními periferními zařízeními, které tyto pokladny nebo kanály používají pro zpracování transakcí. Tato část popisuje každou součást a vysvětluje, jak má být použita při nasazení v maloobchodě.

### <a name="pos-registers"></a>Registry POS

Navigace: Klepněte na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**registruje**. Pokladna POS je entita, která se používá k definování vlastností konkrétní instance POS. Tyto vlastnosti zahrnují hardwarový profil nebo instalační program pro maloobchodní periferní zařízení, které budou použity na rejstříku, úložiště, namapovaný na Žurnál a vizuální zážitek pro uživatele, přihlášení registrovat.

### <a name="devices"></a>Zařízení

Navigace: Klepněte na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**zařízení**. Zařízení je entita, která představuje fyzickou instanci zařízení, která je namapována k pokladně POS. Při vytvoření je zařízení mapováno k pokladně POS. Zařízení sleduje informace o tom, kdy dojde k aktivaci pokladny POS, typu používaného klienta a balíčku aplikace, který byl nasazen na konkrétní zařízení. Zařízení může být dvou typů: **Retail Modern POS** (MPOS) nebo **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS je klientská aplikace POS, která je nainstalována v operačním systému Windows 8.1 nebo novějším pro počítače. Pokud je k zařízení mapován typ aplikace **Retail Modern POS**, lze pro konkrétní zařízení nastavit balíček ke stažení. Balíček ke stažení lze přizpůsobit tak, aby obsahoval různé verze instalačního balíčku. Možnost nasadit různé balíčky poskytuje flexibilitu v případech, kde jiná pokladna POS může vyžadovat různé integrace. MPOS se nasazuje spolu s integrovanou hardwarovou stanicí.

#### <a name="cloud-pos"></a>Shluk POS

Shluk POS je POS se založenou na prohlížeči. Vzhledem k tomu, že běží v prohlížeči, Cloud POS nevyžaduje Windows 8.1 nebo novější operační systém na základě PC. Pokud je k databázovému zařízení mapován typ aplikace **Retail Cloud POS**, dané zařízení lze používat v prohlížeči bez nutnosti stahovat nebo instalovat balíček. Cloud POS vyžaduje hardwarovou stanici, pokud chcete používat jiný hardware, než je skener čárového kódu připojený ke klávesnici.

### <a name="hardware-profile"></a>Profil hardwaru

Navigace: Klepněte na **Commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily**. Profil hardwaru identifikuje hardware, který je připojen k pokladně POS nebo hardwarové stanici. Profil hardwaru slouží také k určení parametrů modulu pro zpracování platby, které mají být použity při komunikaci se sadou SDK (Software Development Kit). (Sada SDK pro platby je nasazena jako součást hardwarové stanice.)

### <a name="hardware-station"></a>Hardwarová stanice

Navigace: Klepněte na **maloobchodní a commerce**&gt;**kanály**&gt;**maloobchodní obchody**&gt;**všechny maloobchodní obchody**. Vyberte obchod a potom klikněte na pevnou záložku **Hardwarové stanice**. Hardwarová stanice je instancí obchodní logiky, která řídí periferie systému POS. Hardwarová stanice je automaticky nainstalována společně s aplikací MPOS. Hardwarovou stanici lze také nainstalovat jako samostatnou součást, a potom k ní získat přístup pomocí řešení MPOS nebo Cloud POS v rámci webové služby. Hardwarová stanice musí být definována na úrovni kanálu.

### <a name="hardware-station-profile"></a>Profil hardwarové stanice

Navigace: Klepněte na **Commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily stanice**. Bez ohledu na to, zda samotná hardwarová stanice na úrovni kanálu obsahuje informace specifické pro instanci, jako je adresa URL hardwarové stanice, profil hardwarové stanice obsahuje informace, které mohou být statické nebo sdíleny v rámci několika hardwarových stanic. Statické informace obsahují port, který má být použit, balíček hardwarové stanice a hardwarový profil. Statické informace obsahuje také popis typu nasazované hardwarové stanice, jako například **Přejít k pokladně **nebo **Vrácení**, a to v závislosti na hardwaru, který je požadován pro každou specifickou hardwarovou stanici.

## <a name="scenarios"></a>Scénáře
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS s připojenými periferními zařízeními

[![Tradiční, stálé místo prodeje](./media/traditional-300x279.png)](./media/traditional.png) MPOS připojit k POS periferie v případě POS tradiční, pevné, nejprve přejděte do rejstříku sám a přiřadit hardwarový profil. Můžete najít Registry POS na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**registruje**. Poté, co jste přiřadili hardwarový profil, proveďte synchronizaci změn s databází kanálu pomocí plánu distribuce „Pokladny“. Můžete najít plány distribuce v **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**. Dále v kanálu nastavte "místní" hardwarovou stanici. Klepněte na tlačítko **maloobchodní a commerce**&gt;**kanály**&gt;**maloobchodní obchody**&gt;**všechny maloobchodní obchody**a vybrat úložiště. Poté na pevné záložce **Hardwarové stanice** kliknutím na tlačítko **Přidat** přidejte hardwarovou stanici. Zadejte popis, zadejte **localhost** jako název hostitele a potom synchronizujte změny s kanálem pomocí plánu distribuce "Konfigurace kanálu". Můžete najít plány distribuce v **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**. Nakonec v aplikaci MPOS pomocí operace **Vybrat hardwarovou stanici** vyberte hardwarovou stanici **localhost**. Nastavte hardwarovou stanici na **Aktivní**. Hardwarový profil, který se používá v tomto případě, by měl vycházet ze samotné pokladny POS. Profil hardwarové stanice není pro tento scénář vyžadován. **Poznámka:** některé změny profilu hardwaru, jako jsou změny do pokladní zásuvky, vyžadují po synchronizaci změn do kanálu otevření nové směny. **Poznámka:** Cloud POS vyžaduje samostatnou hardwarovou stanici ke komunikaci s maloobchodními periferními zařízeními.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS nebo Cloud POS se samostatnou hardwarovou stanicí

\[Titulek id = "Příloha\_340041" Zarovnat = "alignleft" width = "300"\][![sdílené Příslušenství](./media/shared-300x254.png)](./media/shared.png) sdílené Příslušenství\[/titulek\] v tomto případě samostatný hardware stanice je sdílena mezi klienty MPOS a Cloud POS. Tento scénář vyžaduje vytvoření profilu hardwarové stanice a zadání balíčku ke stažení, portu a hardwarový profil, který používá hardwarová stanice. Můžete najít hardwarový profil stanice na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**&gt;**hardwarové profily stanice**. Po vytvoření hardwarového profilu stanice, přejděte do konkrétní maloobchodní síť (**maloobchodní a commerce**&gt;**kanály**&gt;**maloobchodní obchody**&gt;**všechny maloobchodní obchody**) a přidat nový hardware stanice. Namapujte tuto novou hardwarovou stanici k profilu hardwarové stanice, který byl dříve vytvořen. Dále zadejte popis, který pomůže pokladníkovi určit hardwarovou stanici. V **název hostitele** adresa URL hostitele počítače zadejte v následujícím formátu: **https://&lt;MachineName:Port&gt;/HardwareStation**. (Nahradit **&lt;MachineName:Port&gt;** s název skutečné počítače hardware stanice a port, který je určen v hardwarovém profilu stanice.) Pro samostatný hardware stanice měli byste také určit, že že elektronický převod peněžních prostředků (EFT) ID terminálu. Tato hodnota určuje terminál EFT připojený k hardwarové stanici, když konektor platby komunikuje s poskytovatelem platby. Dále ze skutečné hardwarové stanice přejděte na kanál a vyberte hardwarovou stanici. Poté klikněte na tlačítko **Stáhnout** a nainstalujte hardwarovou stanici. V dalším kroku z aplikace MPOS nebo Cloud POS proveďte akci **Vybrat hardwarovou stanici** a vyberte hardwarovou stanici, která byla dříve nainstalována. Vyberte možnost **Pár** a navažte zabezpečené spojení mezi systémem POS a hardwarovou stanicí. Tento krok musí být dokončen jednou pro každou kombinaci systému POS a hardwarové stanice. Po spárování hardwarové stanice se stejná operace používá pro aktivaci hardwarové stanice v době, kdy se používá. V tomto scénáři by měl být hardwarový profil přiřazen profil hardwaru stanice než samotný registr. Pokud z nějakého důvodu nemá hardwarové stanice přímo přiřadit hardwarový profil, hardwarový profil, který je přiřazen k rejstříku používá

## <a name="client-maintenance"></a>Údržba klienta
### <a name="registers"></a>Registry

Pokladny POS jsou spravovány především prostřednictvím samotných pokladen, ale je možné použít také profily, které jsou přiřazeny k pokladnám. Atributy, které jsou specifické pro jednotlivé pokladny, jsou spravovány na úrovni pokladny. Tyto atributy zahrnují úložiště, kde se pokladna používá, číslo pokladny, popis a ID terminálu EFT specifické pro samotnou pokladnu.

### <a name="pos-profiles"></a>Profily POS

Můžete najít profily POS na **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profily POS**. Je vhodné spravovat řadu aspektů pokladny pomocí profilů, protože profily lze sdílet mezi více pokladnami. Profily je možné mapovat buď k individuálním pokladnám, nebo pokud je profil aktivní v rámci celé prodejny, tak k maloobchodu. Následující části popisují profily POS a jejich použití.

#### <a name="offline-profile"></a>Offline profil

Offline profil je nastaven na úrovni obchodu. Slouží ke stanovení nastavení nahrávání pro transakce, které jsou prováděny z pokladen POS, zatímco pokladna není připojena k databázi kanálu.

#### <a name="functionality-profile"></a>Funkční profil

Funkční profil je nastaven na úrovni obchodu. Slouží k určení nastavení na úrovni úložiště informace o funkcích, které lze provádět v POS. Následující možnosti jsou spravovány pomocí funkce profilu. Tyto funkce jsou uspořádány na pevných záložkách.

-   Pevná záložka **Obecné**:
    -   Mezinárodní organizace pro normalizaci (ISO).
    -   Vytvoření odběratele v offline režimu.
    -   Profil s e-mailovou účtenkou.
    -   Centrální ověřování zaměstnanců přihlášením.
-   Pevná záložka **Funkce**:
    -   Správa přihlášení a rozšířeného přihlášení.
    -   Finanční aspekty a aspekty měny systému POS, jako například možnost ručního zadávání cen a to, zda jsou desetinná místa požadována pro vedlejší měny.
    -   Povolení registrace času prostřednictvím systému POS.
    -   Jak se produkty a platby zobrazí v systému POS a na účtenkách.
    -   Správa na konci dne.
    -   Parametry kanálu uchovávání informací o transakci v databázi kanálů.
    -   Jak jsou zákazníci vyhledáváni a vytvářeni ze systému POS.
    -   Jak je vypočtena sleva.
-   Pevná záložka **Částka**:
    -   Maximální a minimální ceny, které jsou povoleny.
    -   Použití a výpočet slevy.
-   Pevná záložka **Informační kódy**:
    -   Všechny aspekty o způsobu správy informační kódy v POS. Další informace naleznete v tématu [informace o kódy](info-codes-retail.md).
-   Pevná záložka **Číslování účtenek**:
    -   Určete číselné masky pro účtenky, které mohou zahrnovat segmenty pro číslo obchodu, číslo terminálu, konstanty, a to, zda jsou informace o prodeji, vratkách, prodejních objednávkách a nabídkách vytištěny v oddělených řadách, nebo zda jsou všechny součástí stejné sekvence.

#### <a name="receipt-profiles"></a>Profily účtenky

Profily účtenky jsou přiřazeny k tiskárnám v rámci profilu hardwaru. Používají se k určení typů účtenek, které jsou vytištěny z konkrétní tiskárny. Profily obsahují nastavení pro formáty účtenky, ale také nastavení určující to, zda je účtenka vždy vytištěna, nebo zda se pokladník táže, zda chce zákazník účtenku vytisknout. Různé tiskárny mohou rovněž používat různé profily účtenky. Například tiskárna 1 je standardní termální tiskárnou pro tisk účtenek, a proto má menší formáty účtenek. Nicméně tiskárna 2 je však tiskárnou pro tisk účtenek v plné velikosti, která se používá k tisku pouze v případě, že zákazník účtenku vyžaduje (účtenka vyžaduje více místa).

#### <a name="hardware-profiles"></a>Profily hardwaru

Hardwarové profily jsou popsány jako součást instalace klienta dříve v tomto článku. Hardwarové profily jsou přiřazeny přímo k pokladně POS nebo k profilu hardwarové stanice. Používají se k určení typů zařízení, které specifická pokladna POS nebo hardwarová stanice používá. Hardwarové profily se používají také k nastavení EFT, které se používá ke komunikaci s platební sadou SDK.

#### <a name="visual-profiles"></a>Vizuální profily

Vizuální profily jsou přiřazeny na úrovni pokladny. Používají se k určení motivu pro konkrétní pokladnu. Profily obsahují nastavení pro typ aplikace, která se používá (MPOS nebo Cloud POS), barvu zvýraznění a motiv, schéma písem, pozadí přihlašovací stránky a pozadí systému POS.

### <a name="custom-fields"></a>Vlastní pole

Můžete vytvořit vlastní pole, chcete-li přidat pole, která nejsou poskytovány mimo pole pro POS. Další informace o použití vlastních polí naleznete v tématu [práce s vlastní pole blogu](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Text jazyka

Pomocí textu v jiném jazyce můžete přepsat výchozí řetězec v systému POS. Chcete-li přepsat řetězec v systému POS, přidejte nový textový řádek v jiném jazyce. Poté zadejte ID, výchozí řetězec, který má být přepsán, a text, který má být zobrazen v systému POS namísto výchozího řetězce.

### <a name="hardware-station-profiles"></a>Profily hardwarové stanice

Profily hardwarové stanice jsou popsány dříve v tomto článku. Používají se k přiřazení informací k hardwarové stanici, které nejsou specifické pro danou instanci.

### <a name="channel-reports-configuration"></a>Konfigurace sestav kanálů

Nastavení sestav, které jsou k dispozici v maloobchodní síti, můžete měnit na stránce **Konfigurace sestav maloobchodní sítě**. Můžete vytvářet nové sestavy pomocí definice XML pro sestavy, nebo přiřadit sestavu ke konkrétní skupině oprávnění v systému POS.

### <a name="devices"></a>Zařízení

Zařízení jsou popsána dříve v tomto článku. Používají se ke správě aktivace konkrétní pokladny POS. Zařízení se také používají k určení aplikace, která se používá pro konkrétní pokladnu, a instalačního balíčku, který má být použit pro instalaci klienta MPOS. Následují stavy aktivace zařízení:

-   **Čeká na zpracování** – zařízení je připraveno k aktivaci.
-   **Aktivováno** – zařízení bylo aktivováno.
-   **Deaktivováno** – zařízení bylo deaktivováno dříve v zadní kanceláři nebo prostřednictvím systému POS.
-   **Zakázáno** – zařízení bylo zakázáno.

Další informace týkající se aktivace zahrnují informaci o tom, který pracovník změnil stav aktivace zařízení, časové razítko aktivace a to, zda byla konfigurace zařízení ověřena.

### <a name="client-data-synchronization"></a>Synchronizace dat klienta

Všechny změny v klientovi POS s výjimkou změn ve stavu aktivace zařízení musí synchronizovány s databázi kanálu, jinak se neprojeví. Chcete-li synchronizovat změny databáze kanálů, přejděte na **maloobchodní a commerce**&gt;**Retail IT**&gt;**plán distribuce**, a spustit plán povinné distribuce. V případě klientských změn spouštějte plány distribuce „Pokladny“ a „Konfigurace kanálu“.


