---
title: Připojení periferních zařízení k pokladnímu místu (POS).
description: Tento článek popisuje postup připojení periferních zařízení k Retail POS.
author: BrianShook
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice
audience: Application User
ms.reviewer: josaw
ms.custom: 92383
ms.assetid: 83f31ea6-f0a2-4501-9d4d-a37b6eec2599
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ffee75e1713c7c9d31b1d023cd055c2f1a3fc43d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897101"
---
# <a name="connect-peripherals-to-the-point-of-sale-pos"></a>Připojení periferních zařízení k pokladnímu místu (POS).

[!include [banner](includes/banner.md)]

Tento článek popisuje postup připojení periferních zařízení k Retail POS.

> [!NOTE]
> Konkrétní pokyny k instalaci naleznete v tématu [Konfigurace a instalace maloobchodní hardwarové stanice](retail-hardware-station-configuration-installation.md) a [Konfigurace, Instalace a aktivace Moderní POS (MPOS)](retail-modern-pos-device-activation.md).

## <a name="key-components"></a>Klíčové komponenty

Několik komponent slouží k definování vztahů mezi úložištěm, pokladním místem (POS) nebo kanálů v rámci obchodu a periferními zařízeními, které tyto pokladny nebo kanály používají pro zpracování transakcí. Tato část popisuje každou součást a vysvětluje, jak má být použita při nasazení v obchodě.

### <a name="pos-registers"></a>Registry POS

Navigace: klikněte na tlačítko **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Pokladny**.

Pokladna POS je entita, která se používá k definování vlastností konkrétní instance POS. Tyto vlastnosti zahrnují hardwarový profil nebo nastavení periferních zařízení, která budou použita na pokladně, obchod, ke kterému je pokladna namapována a vizuální prostředí uživatele, který se k dané pokladně přihlásí.

### <a name="devices"></a>Zařízení

Navigace: klikněte na tlačítko **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Zařízení**.

Zařízení je entita, která představuje fyzickou instanci zařízení, která je namapována k pokladně POS. Při vytvoření je zařízení mapováno k pokladně POS. Zařízení sleduje informace o tom, kdy dojde k aktivaci pokladny POS, typu používaného klienta a balíčku aplikace, který byl nasazen na konkrétní zařízení. Zařízení může být dvou typů: **Retail modern POS** (MPOS) nebo **Retail Cloud POS** (Cloud POS).

#### <a name="mpos"></a>MPOS

MPOS je klientská aplikace POS, která je nainstalována v operačním systému Windows 8.1 nebo novějším pro počítače. Pokud je k zařízení mapován typ aplikace **Retail modern POS**, lze pro konkrétní zařízení nastavit balíček ke stažení. Balíček ke stažení lze přizpůsobit tak, aby obsahoval různé verze instalačního balíčku. Možnost nasadit různé balíčky poskytuje flexibilitu v případech, kde jiná pokladna POS může vyžadovat různé integrace. MPOS se nasazuje spolu s integrovanou hardwarovou stanicí.

#### <a name="cloud-pos"></a>Cloud POS

Cloudové POS je POS založené na prohlížeči. Vzhledem k tomu, že běží v prohlížeči, nevyžaduje Cloud POS operační systém Windows 8.1 nebo novější operační systémy. Pokud je ke konkrétnímu zařízení v modulu Headquarters mapován typ aplikace **Retail Cloud POS**, dané zařízení lze používat v prohlížeči bez nutnosti stahovat nebo instalovat balíček. Cloud POS vyžaduje hardwarovou stanici, pokud chcete používat jiný hardware, než je skener čárového kódu připojený ke klávesnici.

### <a name="hardware-profile"></a>Profil hardwaru

Navigace: Přejděte na **Maloobchodní a velkoobchodní prodej \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**.

Profil hardwaru identifikuje hardware, který je připojen k pokladně POS prostřednictvím integrované nebo sdílené hardwarové stanice. Profil hardwaru slouží také k určení parametrů modulu pro zpracování platby, které mají být použity při komunikaci se sadou SDK (Software Development Kit). Sada SDK pro platby je nasazena jako součást hardwarové stanice.

### <a name="hardware-station"></a>Hardwarová stanice

Navigace: Přejděte do nabídky **Maloobchodní a velkoobchodní prodej \> Kanály \> Obchody \> Všechny obchody**, vyberte obchod a poté vyberte záložku **Hardwarové stanice**.

Hardwarová stanice je instancí obchodní logiky, která řídí periferie systému POS. Hardwarová stanice je automaticky nainstalována společně s aplikací MPOS. Hardwarovou stanici lze také nainstalovat jako samostatnou součást, a potom k ní získat přístup pomocí řešení MPOS nebo Cloud POS v rámci webové služby. Hardwarová stanice musí být definována na úrovni kanálu.

## <a name="scenarios"></a>Scénáře

### <a name="mpos-with-connected-peripheral-devices"></a>MPOS s připojenými periferními zařízeními

[![Tradiční, stálá prodejní místa.](./media/traditional-300x279.png)](./media/traditional.png)

Pokud chcete připojit MPOS k perifernímu zařízení POS v podobě tradičního, stálého řešení POS, přejděte nejprve do samotného rejstříku a přiřaďte k němu hardwarový profil. Pokladny POS naleznete v nabídce **Maloobchodní a velkoobchodní prodej** &gt; **Instalace kanálu** &gt; **Instalace POS** &gt; **Pokladny**. 

Poté, co jste přiřadili hardwarový profil, proveďte synchronizaci změn s databází kanálu pomocí plánu distribuce **Pokladny**. Plány distribuce můžete najít v nabídce **Maloobchodní a velkoobchodní prodej** &gt; **Maloobchodní a velkoobchodní prodej IT** &gt; **Plán distribuce**. 

Dále v kanálu nastavte vyhrazenou hardwarovou stanici. Přejděte do nabídky **Maloobchodní a velkoobchodní prodej \> Kanály \> Obchody \> Všechny obchody** a vyberte obchod. 

Poté na záložce **Hardwarové stanice** vyberte možnost **Přidat** a přidejte hardwarovou stanici. Jako typ hardwarové stanice vyberte možnost **Vyhrazená** a poté zadejte popis. Pole **Hardwarový profil** může zůstat prázdné, protože hardwarový profil použitý v tomto scénáři pochází ze samotné pokladny POS. Pak synchronizujte změny do kanálu pomocí distribučního plánu **Konfigurace kanálu**. Plány distribuce najdete v nabídce **Maloobchodní a velkoobchodní prodej \> Maloobchodní a velkoobchodní prodej IT \> Plán distribuce**. 

Nakonec v MPOS použijte operaci **Vybrat hardwarovou stanici** k výběru hardwarové stanice odpovídající hodnotě, kterou jste dříve zadali v popisu, a nastavte hardwarovou stanici jako **Aktivní**. 

> [!NOTE]
> - Některé změny profilu hardwaru, jako jsou změny do pokladní zásuvky, vyžadují po synchronizaci změn do kanálu otevření nové směny.
> - Cloud POS vyžaduje samostatnou hardwarovou stanici ke komunikaci s periferními zařízeními.

### <a name="mpos-or-cloud-pos-with-a-stand-alone-hardware-station"></a>MPOS nebo Cloud POS se samostatnou hardwarovou stanicí

[![Sdílená periferní zařízení.](./media/shared-300x254.png)](./media/shared.png)

V tomto scénáři je samostatná hardwarová stanice sdílena mezi klienty MPOS a Cloud POS. Tento scénář vyžaduje vytvoření sdílené hardwarové stanice a zadání balíčku ke stažení, portu a hardwarový profil, který používá hardwarová stanice. Novou hardwarovou stanici definujete výběrem záložky **Hardwarové stanice** v konkrétním kanálu (**Maloobchodní a velkoobchodní prodej \> Kanály \> Obchody \> Všechny obchody**) a přidání nové hardwarové stanice typu **Sdílená**. 

Dále zadejte popis, který pomůže pokladníkovi určit hardwarovou stanici. V poli **Název hostitele** zadejte adresu URL hostitelského počítače v následujícím formátu: `https://<MachineName:Port>/HardwareStation`. (Část **&lt;MachineName:Port&gt;** nahraďte skutečným názvem hardwarové stanice a číslem portu.) U samostatné hardwarové stanice byste měli také určit ID terminálu pro elektronický převod peněžních prostředků (EFT). Tato hodnota určuje terminál EFT připojený k hardwarové stanici, když konektor platby komunikuje s poskytovatelem platby. 

Dále z počítače, na kterém bude hostována hardwarová stanice, přejděte na kanál v centrále a vyberte hardwarovou stanici. Poté vyberte příkaz **Stáhnout** a stáhněte instalační program hardwarové stanice a nainstalujte stanici. Další informace o instalaci hardwarové stanice viz [Konfigurace a instalace maloobchodní hardwarové stanice](retail-hardware-station-configuration-installation.md). 

V dalším kroku z aplikace MPOS nebo Cloud POS proveďte akci **Vybrat hardwarovou stanici** a vyberte hardwarovou stanici, která byla dříve nainstalována. Vyberte možnost **Pár** a navažte zabezpečené spojení mezi systémem POS a hardwarovou stanicí. Tento krok musí být dokončen jednou pro každou kombinaci systému POS a hardwarové stanice. 

Po spárování hardwarové stanice se stejná operace používá pro aktivaci hardwarové stanice v době, kdy se používá. V tomto scénáři by měl být hardwarový profil přiřazen ke sdílené hardwarové stanici, nikoli k samotné pokladně. Pokud z nějakého důvodu nemá hardwarová stanice přímo přiřazen žádný hardwarový profil, použije se ten hardwarový profil, který je přiřazen k pokladně.

## <a name="client-maintenance"></a>Údržba klienta

### <a name="registers"></a>Pokladny

Pokladny POS jsou spravovány především prostřednictvím samotných pokladen, ale je možné použít také profily, které jsou přiřazeny k pokladnám. Atributy, které jsou specifické pro jednotlivé pokladny, jsou spravovány na úrovni pokladny. Tyto atributy zahrnují úložiště, kde se pokladna používá, číslo pokladny, popis a ID terminálu EFT specifické pro samotnou pokladnu.

### <a name="pos-profiles"></a>Profily POS

Profily POS naleznete v nabídce **Maloobchodní a velkoobchodní prodej** &gt; **Instalace kanálu** &gt; **Instalace POS** &gt; **Profily POS**. Je vhodné spravovat řadu aspektů pokladny pomocí profilů, protože profily lze sdílet mezi více pokladnami. Profily je možné mapovat buď k individuálním pokladnám, nebo pokud je profil aktivní v rámci celé prodejny, tak k obchodu. Následující části popisují profily POS a jejich použití.

#### <a name="offline-profile"></a>Offline profil

Offline profil je nastaven na úrovni obchodu. Slouží ke stanovení nastavení nahrávání pro transakce, které jsou prováděny z pokladen POS, zatímco pokladna není připojena k databázi kanálu.

#### <a name="functionality-profile"></a>Funkční profil

Funkční profil je nastaven na úrovni obchodu. Slouží ke stanovení nastavení na úrovni obchodu z oblasti funkcí, které lze provádět v systému POS. Následující možnosti jsou spravovány pomocí funkčního profilu. Tyto funkce jsou uspořádány na pevných záložkách.

- Pevná záložka **Obecné**:

    - Mezinárodní organizace pro normalizaci (ISO).
    - Vytvoření odběratele v offline režimu.
    - Profil s e-mailovou účtenkou.
    - Centrální ověřování zaměstnanců přihlášením.

- Pevná záložka **Funkce**:

    - Správa přihlášení a rozšířeného přihlášení.
    - Finanční aspekty a aspekty měny systému POS, jako například možnost ručního zadávání cen a to, zda jsou desetinná místa požadována pro vedlejší měny.
    - Povolení registrace času prostřednictvím systému POS.
    - Jak se produkty a platby zobrazí v systému POS a na účtenkách.
    - Správa na konci dne.
    - Parametry kanálu uchovávání informací o transakci v databázi kanálů.
    - Jak jsou zákazníci vyhledáváni a vytvářeni ze systému POS.
    - Jak je vypočtena sleva.

- Pevná záložka **Částka**:

    - Maximální a minimální ceny, které jsou povoleny.
    - Použití a výpočet slevy.

- Pevná záložka **Informační kódy**:

    - Všechny aspekty toho, jak jsou informační kódy v systému POS spravovány. Další podrobnosti naleznete v tématu [Informační kódy a skupiny informačních kódů](info-codes-retail.md).

- Pevná záložka **Číslování účtenek**:

    - Určete číselné masky pro účtenky, které mohou zahrnovat segmenty pro číslo obchodu, číslo terminálu, konstanty, a to, zda jsou informace o prodeji, vratkách, prodejních objednávkách a nabídkách vytištěny v oddělených řadách, nebo zda jsou všechny součástí stejné sekvence.

#### <a name="receipt-profiles"></a>Profily účtenky

Profily účtenky jsou přiřazeny k tiskárnám v rámci profilu hardwaru. Používají se k určení typů účtenek, které jsou vytištěny z konkrétní tiskárny. Profily obsahují nastavení pro formáty účtenky, ale také nastavení určující to, zda je účtenka vždy vytištěna, nebo zda se pokladník táže, zda chce zákazník účtenku vytisknout. Různé tiskárny mohou rovněž používat různé profily účtenky. Například tiskárna 1 je standardní termální tiskárnou pro tisk účtenek, a proto má menší formáty účtenek. Nicméně tiskárna 2 je však tiskárnou pro tisk účtenek v plné velikosti, která se používá k tisku pouze v případě, že zákazník účtenku vyžaduje (účtenka vyžaduje více místa). Další informace naleznete v tématu [Konfigurace profilu příjemek](configure-emailed-receipt-formats.md#configure-a-receipt-profile).

#### <a name="hardware-profiles"></a>Profily hardwaru

Hardwarové profily jsou popsány jako součást instalace klienta dříve v tomto článku. Hardwarové profily jsou přiřazeny přímo pokladně POS nebo sdílené hardwarové stanici a používají se k určení typů zařízení, které konkrétní pokladna POS nebo hardwarová stanice používá. Hardwarové profily se používají také k nastavení EFT, které se používá ke komunikaci s platební sadou SDK.

#### <a name="visual-profiles"></a>Vizuální profily

Vizuální profily se používají k určení motivu pro konkrétní pokladnu, a jsou přiřazeny na úrovni registru. Profily obsahují nastavení pro typ aplikace, která se používá (MPOS nebo Cloud POS), barvu zvýraznění a motiv, schéma písem, pozadí přihlašovací stránky a pozadí systému POS. Další informace viz [Vytváření vizuálních profilů pokladních míst (POS)](tasks/create-pos-visual-profile-2016-02.md). 

### <a name="custom-fields"></a>Vlastní pole

Chcete-li přidat pole, která nejsou standardně v systému POS poskytována, můžete vytvořit pole vlastní. Další informace o použití vlastních polí naleznete v tématu [Práce s příspěvky s vlastními poli](https://blogs.msdn.microsoft.com/axsupport/2012/08/06/ax-for-retail-2012-working-with-custom-fields/).

### <a name="language-text"></a>Text jazyka

Pomocí textu v jiném jazyce můžete přepsat výchozí řetězec v systému POS. Chcete-li přepsat řetězec v systému POS, přidejte nový textový řádek v jiném jazyce. Poté zadejte ID, výchozí řetězec, který má být přepsán, a text, který má být zobrazen v systému POS namísto výchozího řetězce.

### <a name="channel-reports-configuration"></a>Konfigurace sestav kanálů

Nastavení sestav, které jsou k dispozici v kanálu, můžete měnit na stránce **Konfigurace sestav kanálů**. Můžete vytvářet nové sestavy pomocí definice XML pro sestavy, nebo přiřadit sestavu ke konkrétní skupině oprávnění v systému POS.

### <a name="devices"></a>Zařízení

Zařízení jsou popsána dříve v tomto článku. Používají se ke správě aktivace konkrétní pokladny POS. Zařízení se také používají k určení aplikace, která se používá pro konkrétní pokladnu, a instalačního balíčku, který má být použit pro instalaci klienta MPOS. Následují stavy aktivace zařízení:

- **Čeká na zpracování** – zařízení je připraveno k aktivaci.
- **Aktivováno** – zařízení bylo aktivováno.
- **Deaktivováno** – zařízení bylo deaktivováno buď v modulu Headquarters nebo prostřednictvím systému POS.
- **Zakázáno** – zařízení bylo zakázáno.

Další informace týkající se aktivace zahrnují informaci o tom, který pracovník změnil stav aktivace zařízení, časové razítko aktivace a to, zda byla konfigurace zařízení ověřena.

### <a name="client-data-synchronization"></a>Synchronizace dat klienta

Všechny změny v klientu POS s výjimkou změn ve stavu aktivace zařízení musí synchronizovány s databázi kanálu, jinak se neprojeví. Chcete-li synchronizovat změny s databází kanálů, přejděte do nabídky **Maloobchodní a velkoobchodní prodej** &gt; **Maloobchodní a velkoobchodní prodej IT** &gt; **Plán distribuce** a spusťte požadovaný plán distribuce. V případě klientských změn spouštějte plány distribuce **Pokladny** a **Konfigurace kanálu**.

## <a name="additional-resources"></a>Další prostředky

[Konfigurace a instalace Retail Hardware Station](retail-hardware-station-configuration-installation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
