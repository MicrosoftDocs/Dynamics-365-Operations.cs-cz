---
title: Zpracování refundace platby v kontaktních střediscích
description: Toto téma vysvětluje, jak se refundace plateb generují prostřednictvím call center, když se vytvářejí vrácené položky nebo když se ruší objednávky nebo řádky objednávek.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 130f570646d73e37a790ab90ae9a1d6a48b0f8b8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351362"
---
# <a name="refund-payment-processing-in-call-centers"></a>Zpracování refundace platby v kontaktních střediscích

Toto téma vysvětluje, jak se refundace plateb generují prostřednictvím call center, když se vytvářejí vrácené položky nebo když se ruší objednávky nebo řádky objednávek.

Uživatel, který vytvoří objednávku vrácení pro zákazníka jako uživatel call centra v ústředí Microsoft Dynamics 365 Commerce, používá stránku **Vrátit objednávku** k vytvoření počáteční autorizace vrácených materiálů (RMA). RMA definuje produkty, které chce zákazník vrátit nebo vyměnit, a vytváří propojenou prodejní objednávku vrácení, která má typ objednávky **Vrácená objednávka**. Tato propojená vrácená objednávka se používá ke sledování zaúčtování vráceného zboží a veškerých dobropisů nebo vrácení plateb, které jsou zaúčtovány.

Pokud je možnost **Povolit dokončení objednávky** nastavena na **Ano** pro kanál call centra, musí uživatel call centra, který vytvoří RMA, spustit postup zpracování dokončení objednávky výběrem **Dokončit** na stránce **Vrátit objednávku**. Funkce **Dokončit** poskytuje vypočítané shrnutí návratnosti, které zobrazuje přehled splatné částky refundace. Pokud je navíc správně nakonfigurován, systematicky vytvoří řádek platby refundace proti vrácené objednávce.

Logika call centra určuje platební metodu pro řádek platby refundace na základě platební metody, která byla použita pro původní objednávku. Pokud vytvořená objednávka vrácení není spojena s původní objednávkou, použije se výchozí platební metoda převzatá ze systémového parametru.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Jak call centrum určuje, který způsob platby se má použít na příkaz k vrácení

Call centrum používá platební metodu původní objednávky k určení platební metody, která má být použita na návratovou objednávku. Takto funguje tento proces u následujících původních platebních metod:

- **Normální** (hotovost) nebo **Šek** – Když vytvořená vrácená objednávka odkazuje na původní objednávku, která byla zaplacena pomocí běžného (hotovostního) nebo šekového typu platby, aplikace call centra odkazuje na konfigurace na stránce **Způsoby refundace v call centru**. Tato stránka umožňuje organizacím definovat podle měny objednávek, jak budou vráceny platby zákazníkům za objednávky, které byly původně zaplaceny pomocí běžného typu platby nebo šeku. Stránka **Metody refundace v call centru** také umožňuje organizacím vybrat, zda se zákazníkovi odešle šek pro vrácení peněz vygenerovaný systémem, nebo zda se na interním zůstatku zákaznického účtu vytvoří kredit na účet zákazníka. V těchto scénářích logika call centra odkazuje na měnu objednávky vrácení a poté použije hodnotu **Maloobchodní platební metoda** pro tuto měnu k vytvoření řádku vrácení platby na prodejní objednávce vrácení. Později je k měně propojen deník plateb pohledávek zákazníků (AR), který používá mapovanou platební metodu AR.

    Následující obrázek ukazuje konfiguraci pro scénář, kdy zákazník vrátí produkty z prodejní objednávky, která je propojena s měnou USD a která byla původně zaplacena pomocí běžného nebo šekového typu platby. V tomto scénáři bude zákazníkovi vrácena refundace prostřednictvím šeku refundace generovaného systémem. Způsob platby AR **REF-CHK** byl nakonfigurován jako typ platby šeku pro refundaci.

    ![Konfigurace metod refundace call centra pro normální a šekové původní platby.](media/callcenterrefundmethods.png)

- **Kreditní karta** – Když vytvořená návratová objednávka odkazuje na původní objednávku, která byla zaplacena pomocí kreditní karty, použije logika call centra pro platby vrácení stejnou původní kreditní kartu na objednávku vrácení.
- **Věrnostní karta** – Když vytvořená návratová objednávka odkazuje na původní objednávku, která byla zaplacena pomocí zákaznické věrnostní karty, použije logika call centra pro platby vrácení stejnou věrnostní kartu.
- **Dárková karta** (interní) – Když vytvořená vrácená objednávka odkazuje na původní objednávku, která byla zaplacena pomocí dárkové karty, která byla vydána z Dynamics 365 Commerce (funkce interní dárkové karty), logika call centra pro platby refundací vrátí peníze na stejné původní číslo dárkové karty.
- **Dárková karta** (externí) – Když vytvořená objednávka vrácení odkazuje na původní objednávku, která byla zaplacena pomocí externí dárkové karty třetí strany, použije logika call centra pro platby refundace výchozí způsob platby refundace, který je definován na kartě **RMA/vrácení** stránky **Parametry call centra**.

Pokud je z jakéhokoli důvodu neznámý typ platby původní objednávky nebo pokud bylo k úhradě původní objednávky použito více platebních metod, použije logika call centra výchozí platební metodu vrácení, která je definována na kartě **RMA/vrácení** stránky **Parametry call centra**.

Následující obrázek ukazuje pole **Způsob platby** na kartě **RMA/vrácení** stránky **Parametry call centra**.

![Pole Způsob platby na kartě RMA/vrácení stránky Parametry call centra.](media/callcenterrefundparameters.png)

> [!NOTE]
> Pravidla zpracování refundace, která jsou popsána výše, platí také pro objednávky nebo řádky objednávek, které uživatel call centra zruší v ústředí Commerce. Pokud zrušení objednávky nebo konkrétních řádků objednávky způsobí jakékoli přeplatky, použijí se ke generování řádků platby refundace stejná pravidla.

Obvykle objednávka vrácení prochází standardním procesem, kdy je přijato (nebo zlikvidováno) zboží, je zaúčtován dodací list proti objednávce vrácení a poté je spuštěn proces zaúčtování faktury pro prodejní objednávku vrácení. Prodejní objednávka vrácení je propojena a systematicky generována jako součást procesu vytváření objednávky vrácení. V typických scénářích se refundace plateb nevydávají zákazníkům, dokud není zaúčtována faktura za prodejní objednávku vrácení.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Co se stane, když je faktura zaúčtována na prodejní objednávku vrácení

Následující scénáře vysvětlují, co se stane, když je faktura zaúčtována na prodejní objednávku vrácení:

- Pokud je refundace platby v objednávce vrácení na kreditní kartu, je při zaúčtování faktury vyvolána další logika. Tato logika volá zpracovatele plateb, aby vrátil platbu na kreditní kartu zákazníka. Je také vytvořen poukaz zákazníka na vrácení peněz a systematicky zaúčtován na účet zákazníka. Tento deník plateb bude zúčtován na poukázku dobropisu na vrácenou objednávku.
- Pokud je platba refundace, která musí být vystavena, pro typ platby šekem, je vytvořen platební poukaz zákazníka, který používá platební metodu AR, a musí být ručně zaúčtován nebo vytištěn, než bude možné platební poukaz zaúčtovat na účet zákazníka. Ke zpracování kontroly vrácení peněz mohou uživatelé použít stránku **Deník plateb zákazníka** v Pohledávkách nebo specializovanou stránku **Zpracování šeku refundace** v Retail a Commerce.
- Pokud je platba refundace, která musí být vystavena, pro typ platby interní dárkové karty nebo věrnostní karty, je při fakturaci objednávky vrácení vytvořen poukaz na vrácení platby a zaúčtován na účet zákazníka. Tento krok fakturace také přidá částku vrácení zpět k interně sledovanému zůstatku zákazníka na dárkové kartě nebo zůstatku věrnostních bodů.
- Pokud platební metoda, která používá funkci **Zákazník** (například zákaznický účet), je spojena s prodejní objednávkou vrácení, ověření kreditního limitu je při zpracování platby ignorováno. V této souvislosti není vytvořen ani zveřejněn žádný platební poukaz. Pokud je na objednávce pro vrácení použit typ platby zákazníka, slouží doklad o dobropisu, který vytvoří proces zaúčtování faktury, jako doklad o kreditu zákazníka a označuje vrácení zůstatku AR zákazníka.

## <a name="advance-credit"></a>Zálohový kredit

Když uživatel zpracovává vrácené objednávky jako uživatel call centra v call centru, kde je možnost **Povolit dokončení objednávky** nastavena na **Ano**, může dojít k výjimce z dříve popsaného procesu pro zaúčtování platby vrácení peněz, pokud uživatel call centra, který vytváří objednávku vrácení, nastaví možnost **Záloha předem** na **Ano** na kartě **RMA/vrácení** stránky **Parametry call centra**. V takovém případě dojde k vrácení platby okamžitě po úspěšném odeslání objednávky vrácení pomocí funkce **Odeslat** funkce na stránce **Souhrn vrácení**. Systém okamžitě vytvoří poukaz zákazníka na platbu předem na vrácenou hodnotu, přestože samotná prodejní objednávka vrácení ještě nebyla fakturována. Tento přístup lze použít v situacích, kdy organizace musí vydat vrácení peněz zákazníkům předem kvůli problémům se zákaznickými službami a nechce požadovat přijetí vráceného zboží před vydáním refundace.

## <a name="replacement-orders"></a>Objednávky náhrady

Při vystavení příkazu k vrácení se funkce **Objednávka náhrady** dá použít ke generování nové prodejní objednávky pro zákazníka. Tento přístup lze použít ve scénářích výměny. Funkce **Objednávka náhrady** vytvoří další prodejní objednávku pro nové položky, které musí být odeslány, ale křížový odkaz na kartu **RMA/vrácení** stránky **Parametry call centra** propojuje objednávku na výměnu, RMA a prodejní objednávku vrácení.

Při zpracování plateb za objednávku náhrady mají organizace dvě možnosti:

- Refundovat zákazníkovi objednávku vrácení na základě původní platební metody a poté vyzvednutí samostatné platby za objednávku náhrady. K použití této možnosti není nutná žádná další konfigurace.
- Nastavte možnost **Použít kredit** na **Ano** na kartě **RMA/vrácení** stránky **Parametry call centra**. V takovém případě se zákaznická platební metoda systematicky použije jak na objednávku vrácení, tak na objednávku výměny. Tato možnost pomůže zabránit vystavení externí platby refundace. Pomáhá také zabránit zpracování plateb v transakci. Může to být užitečné v situacích, kdy se zpracovává rovná směna a organizace upřednostňuje použití dobropisu, který je generován při fakturaci objednávky vrácení k úhradě faktury, která je generována objednávkou náhrady. Když je možnost **Použít kredit** nastavena na **Ano**, musí organizace po vygenerování obou těchto finančních dokladů ručně vyrovnat dobropis proti faktuře objednávky náhrady.

Nastavení **Ano** pro možnost **Použít kredit** je k dispozici pouze v případě, že bude objednávka vrácení spojena s objednávkou náhrady. V tomto případě je platební metoda zákazníka, která bude použita k systematické platbě za objednávku vrácení a výměny , definována polem **Použít platební metodu kreditů** na kartě **RMA/vrácení** stránky **Parametry call centra**. V tomto poli lze vybrat pouze platbu typu platby funkce **Zákazník**.

> [!NOTE]
> Pro objednávku vrácení, která nemá žádnou propojenou objednávku výměny, nastavení **Ano** u možnosti **Použít kredit** nebude mít žádný vliv na platební logiku objednávky vrácení, protože toto nastavení se vztahuje pouze na objednávky náhrady.

![Použití pole způsobu platby kreditu na kartě RMA/vrácení stránky Parametry call centra.](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Pokud uživatelé, kteří vytvářejí objednávky náhrady, plánují použít možnost **Použít kredit**, neměli by spouštět funkci **Dokončit** na objednávce vrácení, než nastaví možnost **Použít kredit** na **Ano**. Po spuštění funkce **Dokončit** je platba refundace vypočítána a použita na prodejní objednávku vrácení. Jakýkoli pokus o nastavení možnost **Použít kredit** na **Ano** poté, co již byla vypočítána a použita platba refundace, nespustí přepočet platby refundace a platební metoda, která je vybrána v poli **Použít platební metodu kreditů** nebude použita. Pokud je třeba v tomto kontextu potřeba použít možnost **Použít kredit**, uživatel musí odstranit objednávku náhrady a RMA a poté začít znovu a vytvořit nové RMA. Tentokrát musí uživatel zajistit, aby byla možnost **Použít kredit** nastavena na **Ano** před spuštění funkce **Dokončit**.

## <a name="payment-overrides-for-call-center-returns"></a>Přepíše platby za vrácení z call centra

Ačkoli logika call centra systematicky určuje způsob platby refundace způsobem popsaným výše v tomto tématu, uživatelé někdy mohou chtít tyto platby přepsat. Uživatel může například upravit nebo odebrat stávající řádky platby pro refundaci a použít nové řádky platby. Systémem vypočítané platby refundace mohou změnit pouze uživatelé, kteří mají správná přepisovací oprávnění. Tato oprávnění lze konfigurovat na stránce **Přepsat oprávnění** v Retail a Commerce. Chcete-li provést přepsání platby refundace, musí být uživatel propojen s rolí zabezpečení, kde je možnost **Povolit alternativní platbu** nastavena na **Ano** na stránce **Přepsat oprávnění**.

![Povolení alternativních možností platby na stránce Přepsat oprávnění.](media/overridepermissions.png)

Alternativně může organizace nastavit možnost **Povolit přepsání plateb** na **Ano** na kartě **RMA/vrácení** stránky **Parametry call centra**. V takovém případě musí být v kód přepsání zabezpečení vybrán v poli **Kód přepsání zabezpečení**. Kód přepsání zabezpečení je alfanumerický kód, který musí být spravován externě, protože uživatelé jej po nastavení nemohou zobrazit v Commerce. Kód přepsání zabezpečení by mělo znát jen několik klíčových důvěryhodných lidí v organizaci. Když je možnost **Povolit přepsání plateb** nastavena na **Ano** a uživatelé, kteří nemají správná oprávnění role, se pokusí změnit způsob platby na objednávce vrácení, budou mít možnost zadat kód přepsání zabezpečení. Pokud to nevědí nebo pokud to pro ně manažer nebo vedoucí na stránce nemůže zadat, nebudou moci přepsat způsob platby vrácení.

> [!NOTE]
> Pokud je kód přepsání zabezpečení ztracen nebo zapomenut, organizace ho bude muset resetovat definováním nového kódu přepsání zabezpečení v poli **Kód přepsání zabezpečení** na kartě **RMA/vrácení** stránky **Parametry call centra**.

![Parametry přepsání platby na kartě RMA/vrácení stránky Parametry call centra.](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Než se organizace pokusí přepsat platby refundace, které používají typy plateb kreditní kartou, musí ověřit, zda jejich zpracovatel kreditní karty umožňuje nepřipojené vrácení. Mnoho zpracovatelů požaduje vrácení peněz zpět na původní kartu. Jakýkoli pokus o refundaci peněz na kartu, která nemá žádné předchozí zachycení, může způsobit selhání odesílání u zpracovatele.

## <a name="additional-resources"></a>Další prostředky

[Platební metody v kontaktních střediscích](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]