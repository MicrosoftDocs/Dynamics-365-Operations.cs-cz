---
title: "Definování a správa klientů z obchodních kanálů, pokladen a hardwarových stanic"
description: "Toto téma popisuje postup připojení periferních zařízení k vaší pokladně POS."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: efce1a6f8b87cbaebcf4436e33e832d49a040329
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="define-and-maintain-channel-clients-registers-and-hardware-stations"></a>Definování a správa klientů z obchodních kanálů, pokladen a hardwarových stanic

[!INCLUDE [banner](includes/banner.md)]

Toto téma popisuje postup připojení periferních zařízení k vaší pokladně POS.

**Poznámka:** konkrétní pokyny k instalaci naleznete v tématu [Konfigurace a instalace hardwarové stanice pro maloobchod](retail-hardware-station-configuration-installation.md) a [Samoobslužné stažení/instalace řešení Retail Modern POS a aktivace zařízení Modern POS a Cloud POS](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Klíčové komponenty
Několik komponent slouží k definování vztahů mezi úložištěm, pokladním místem (POS) nebo kanálů v rámci obchodu a maloobchodními periferními zařízeními, které tyto pokladny nebo kanály používají pro zpracování transakcí. Tato část popisuje každou součást a vysvětluje, jak má být použita při nasazení v maloobchodě.

### <a name="pos-registers"></a>Registry POS

Navigace: klikněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Pokladny**. Pokladna POS je entita, která se používá k definování vlastností konkrétní instance POS. Tyto vlastnosti zahrnují hardwarový profil nebo nastavení maloobchodních periferních zařízení, která budou použita na pokladně, obchod, ke kterému je pokladna namapována a vizuální prostředí uživatele, který se k dané pokladně přihlásí.

### <a name="devices"></a>Zařízení

Navigace: klikněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Zařízení**. Zařízení je entita, která představuje fyzickou instanci zařízení, která je namapována k pokladně POS. Při vytvoření je zařízení mapováno k pokladně POS. Zařízení sleduje informace o tom, kdy dojde k aktivaci pokladny POS, typu používaného klienta a balíčku aplikace, který byl nasazen na konkrétní zařízení. Zařízení může být dvou typů: **Retail Modern POS** (MPOS) nebo **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS je klientská aplikace POS, která je nainstalována v operačním systému Windows 8.1 nebo novějším pro počítače. Pokud je k zařízení mapován typ aplikace **Retail Modern POS**, lze pro konkrétní zařízení nastavit balíček ke stažení. Balíček ke stažení lze přizpůsobit tak, aby obsahoval různé verze instalačního balíčku. Možnost nasadit různé balíčky poskytuje flexibilitu v případech, kde jiná pokladna POS může vyžadovat různé integrace. MPOS se nasazuje spolu s integrovanou hardwarovou stanicí.

#### <a name="cloud-pos"></a>Cloud POS

Cloudové POS je POS založené na prohlížeči. Vzhledem k tomu, že běží v prohlížeči, nevyžaduje Cloud POS operační systém Windows 8.1 nebo novější operační systémy. Pokud je ke konkrétnímu zařízení v modulu Retail headquarters mapován typ aplikace **Retail Cloud POS**, dané zařízení lze používat v prohlížeči bez nutnosti stahovat nebo instalovat balíček. Cloud POS vyžaduje hardwarovou stanici, pokud chcete používat jiný hardware, než je skener čárového kódu připojený ke klávesnici.

### <a name="hardware-profile"></a>Profil hardwaru

Navigace: klikněte na **Velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Hardwarové profily**. Profil hardwaru identifikuje hardware, který je připojen k pokladně POS nebo hardwarové stanici. Profil hardwaru slouží také k určení parametrů modulu pro zpracování platby, které mají být použity při komunikaci se sadou SDK (Software Development Kit). (Sada SDK pro platby je nasazena jako součást hardwarové stanice.)

### <a name="hardware-station"></a>Hardwarová stanice

Navigace: klikněte na **Retail** &gt; **Kanály** &gt; **Maloobchody** &gt; **Všechny maloobchody**. Vyberte obchod a potom klikněte na pevnou záložku **Hardwarové stanice**. Hardwarová stanice je instancí obchodní logiky, která řídí periferie systému POS. Hardwarová stanice je automaticky nainstalována společně s aplikací MPOS. Hardwarovou stanici lze také nainstalovat jako samostatnou součást, a potom k ní získat přístup pomocí řešení MPOS nebo Cloud POS v rámci webové služby. Hardwarová stanice musí být definována na úrovni kanálu.

### <a name="hardware-station-profile"></a>Profil hardwarové stanice

Navigace: klikněte na **Velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Profily hardwarové stanice**. Bez ohledu na to, zda samotná hardwarová stanice na úrovni kanálu obsahuje informace specifické pro instanci, jako je adresa URL hardwarové stanice, profil hardwarové stanice obsahuje informace, které mohou být statické nebo sdíleny v rámci několika hardwarových stanic. Statické informace obsahují port, který má být použit, balíček hardwarové stanice a hardwarový profil. Statické informace obsahuje také popis typu nasazované hardwarové stanice, jako například **Přejít k pokladně** nebo **Vrácení**, a to v závislosti na hardwaru, který je požadován pro každou specifickou hardwarovou stanici.

## <a name="scenarios"></a>Scénáře
### <a name="mpos-with-connected-peripheral-devices"></a>MPOS s připojenými periferními zařízeními

[![Tradiční, stálá prodejní místa](./media/traditional-300x279.png)](./media/traditional.png) 

Pokud chcete připojit MPOS k perifernímu zařízení POS v podobě tradičního, stálého řešení POS, přejděte nejprve do samotného rejstříku a přiřaďte k němu hardwarový profil. Pokladny POS naleznete v nabídce **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Pokladny**. Poté, co jste přiřadili hardwarový profil, proveďte synchronizaci změn s databází kanálu pomocí plánu distribuce „Pokladny“. Plány distribuce můžete najít v nabídce **Retail** &gt; **IT pro maloobchod** &gt; **Plán distribuce**. Dále v kanálu nastavte "místní" hardwarovou stanici. Klikněte na **Retail** &gt; **Kanály** &gt; **Maloobchody** &gt; **Všechny maloobchody** a vyberte obchod. Poté na pevné záložce **Hardwarové stanice** kliknutím na tlačítko **Přidat** přidejte hardwarovou stanici. Zadejte popis, zadejte **localhost** jako název hostitele a potom synchronizujte změny s kanálem pomocí plánu distribuce "Konfigurace kanálu". Plány distribuce můžete najít v nabídce **Retail** &gt; **IT pro maloobchod** &gt; **Plán distribuce**. Nakonec v aplikaci MPOS pomocí operace **Vybrat hardwarovou stanici** vyberte hardwarovou stanici **localhost**. Nastavte hardwarovou stanici na **Aktivní**. Hardwarový profil, který se používá v tomto případě, by měl vycházet ze samotné pokladny POS. Profil hardwarové stanice není pro tento scénář vyžadován. **Poznámka:** některé změny profilu hardwaru, jako jsou změny do pokladní zásuvky, vyžadují po synchronizaci změn do kanálu otevření nové směny. **Poznámka:** Cloud POS vyžaduje samostatnou hardwarovou stanici ke komunikaci s maloobchodními periferními zařízeními.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS nebo Cloud POS se samostatnou hardwarovou stanicí
[![Sdílená periferní zařízení](./media/shared-300x254.png)](./media/shared.png)

V tomto scénáři je samostatná hardwarová stanice sdílena mezi klienty MPOS a Cloud POS. Tento scénář vyžaduje vytvoření profilu hardwarové stanice a zadání balíčku ke stažení, portu a hardwarový profil, který používá hardwarová stanice. Profil hardwarové stanice naleznete v části **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Profily hardwarové stanice**. Po vytvoření profilu hardwarové stanice přejděte do konkrétního maloobchodního kanálu (**Retail** &gt; **Kanály** &gt; **Maloobchody** &gt; **Všechny maloobchody**) a přidejte novou hardwarovou stanici. Namapujte tuto novou hardwarovou stanici k profilu hardwarové stanice, který byl dříve vytvořen. Dále zadejte popis, který pomůže pokladníkovi určit hardwarovou stanici. V poli **Název hostitele** zadejte adresu URL hostitelského počítače v následujícím formátu: **https://&lt;MachineName:Port&gt;/HardwareStation**. (**&lt;MachineName:Port&gt;** nahraďte za skutečný název hardwarové stanice a za port, který je určen v profilu hardwarové stanice.) Pro samostatnou hardwarovou stanici byste měli také určit ID terminálu pro elektronický převod peněžních prostředků (EFT). Tato hodnota určuje terminál EFT připojený k hardwarové stanici, když konektor platby komunikuje s poskytovatelem platby. Dále ze skutečné hardwarové stanice přejděte na kanál a vyberte hardwarovou stanici. Poté klikněte na tlačítko **Stáhnout** a nainstalujte hardwarovou stanici. V dalším kroku z aplikace MPOS nebo Cloud POS proveďte akci **Vybrat hardwarovou stanici** a vyberte hardwarovou stanici, která byla dříve nainstalována. Vyberte možnost **Pár** a navažte zabezpečené spojení mezi systémem POS a hardwarovou stanicí. Tento krok musí být dokončen jednou pro každou kombinaci systému POS a hardwarové stanice. Po spárování hardwarové stanice se stejná operace používá pro aktivaci hardwarové stanice v době, kdy se používá. V tomto scénáři by měl být hardwarový profil přiřazen k profilu hardwarové stanice, nikoli k samotné pokladně. Pokud z nějakého důvodu nemá hardwarová stanice přímo přiřazený hardwarový profil, používá se hardwarový profil, který je přiřazen k pokladně.

## <a name="client-maintenance"></a>Údržba klienta
### <a name="registers"></a>Registry

Pokladny POS jsou spravovány především prostřednictvím samotných pokladen, ale je možné použít také profily, které jsou přiřazeny k pokladnám. Atributy, které jsou specifické pro jednotlivé pokladny, jsou spravovány na úrovni pokladny. Tyto atributy zahrnují úložiště, kde se pokladna používá, číslo pokladny, popis a ID terminálu EFT specifické pro samotnou pokladnu.

### <a name="pos-profiles"></a>Profily POS

Profily POS naleznete v nabídce **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS**. Je vhodné spravovat řadu aspektů pokladny pomocí profilů, protože profily lze sdílet mezi více pokladnami. Profily je možné mapovat buď k individuálním pokladnám, nebo pokud je profil aktivní v rámci celé prodejny, tak k maloobchodu. Následující části popisují profily POS a jejich použití.

#### <a name="offline-profile"></a>Offline profil

Offline profil je nastaven na úrovni obchodu. Slouží ke stanovení nastavení nahrávání pro transakce, které jsou prováděny z pokladen POS, zatímco pokladna není připojena k databázi kanálu.

#### <a name="functionality-profile"></a>Funkční profil

Funkční profil je nastaven na úrovni obchodu. Slouží ke stanovení nastavení na úrovni obchodu z oblasti funkcí, které lze provádět v systému POS. Následující možnosti jsou spravovány pomocí funkčního profilu. Tyto funkce jsou uspořádány na pevných záložkách.

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
    -   Všechny aspekty toho, jak jsou informační kódy v systému POS spravovány. Další informace naleznete v tématu [Informační kódy](info-codes-retail.md).
-   Pevná záložka **Číslování účtenek**:
    -   Určete číselné masky pro účtenky, které mohou zahrnovat segmenty pro číslo obchodu, číslo terminálu, konstanty, a to, zda jsou informace o prodeji, vratkách, prodejních objednávkách a nabídkách vytištěny v oddělených řadách, nebo zda jsou všechny součástí stejné sekvence.

#### <a name="receipt-profiles"></a>Profily účtenky

Profily účtenky jsou přiřazeny k tiskárnám v rámci profilu hardwaru. Používají se k určení typů účtenek, které jsou vytištěny z konkrétní tiskárny. Profily obsahují nastavení pro formáty účtenky, ale také nastavení určující to, zda je účtenka vždy vytištěna, nebo zda se pokladník táže, zda chce zákazník účtenku vytisknout. Různé tiskárny mohou rovněž používat různé profily účtenky. Například tiskárna 1 je standardní termální tiskárnou pro tisk účtenek, a proto má menší formáty účtenek. Nicméně tiskárna 2 je však tiskárnou pro tisk účtenek v plné velikosti, která se používá k tisku pouze v případě, že zákazník účtenku vyžaduje (účtenka vyžaduje více místa).

#### <a name="hardware-profiles"></a>Profily hardwaru

Hardwarové profily jsou popsány jako součást instalace klienta dříve v tomto článku. Hardwarové profily jsou přiřazeny přímo k pokladně POS nebo k profilu hardwarové stanice. Používají se k určení typů zařízení, které specifická pokladna POS nebo hardwarová stanice používá. Hardwarové profily se používají také k nastavení EFT, které se používá ke komunikaci s platební sadou SDK.

#### <a name="visual-profiles"></a>Vizuální profily

Vizuální profily jsou přiřazeny na úrovni pokladny. Používají se k určení motivu pro konkrétní pokladnu. Profily obsahují nastavení pro typ aplikace, která se používá (MPOS nebo Cloud POS), barvu zvýraznění a motiv, schéma písem, pozadí přihlašovací stránky a pozadí systému POS.

### <a name="custom-fields"></a>Vlastní pole

Chcete-li přidat pole, která nejsou standardně v systému POS poskytována, můžete vytvořit pole vlastní. Další informace o použití vlastních polí naleznete v tématu [Práce s příspěvky s vlastními poli](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

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
-   **Deaktivováno** – zařízení bylo deaktivováno buď v modulu Retail headquarters nebo prostřednictvím systému POS.
-   **Zakázáno** – zařízení bylo zakázáno.

Další informace týkající se aktivace zahrnují informaci o tom, který pracovník změnil stav aktivace zařízení, časové razítko aktivace a to, zda byla konfigurace zařízení ověřena.

### <a name="client-data-synchronization"></a>Synchronizace dat klienta

Všechny změny v klientovi POS s výjimkou změn ve stavu aktivace zařízení musí synchronizovány s databázi kanálu, jinak se neprojeví. Chcete-li synchronizovat změny s databází kanálů, přejděte do nabídky **Retail** &gt; **IT pro maloobchod** &gt; **Plán distribuce** a spusťte požadovaný plán distribuce. V případě klientských změn spouštějte plány distribuce „Pokladny“ a „Konfigurace kanálu“.




