---
title: Dodavatelská spolupráce s externími dodavateli
description: Tento článek vysvětluje, jak nákupčí mohou spolupracovat s externími dodavateli na výměně informací o nákupních objednávkách a zásobách dodávek.
author: GalynaFedorova
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart, PurchaseOrderResponseActionRemarks, PurchVendorPortalAllResponse, PurchOrderInExternalReview, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 25561802996514f6f60fc9400c22dc61a30ef1c8
ms.sourcegitcommit: bad64015da0c96a6b5d81e389708281406021d4f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023781"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Dodavatelská spolupráce s externími dodavateli

[!include [banner](../includes/banner.md)]

Modul **Spolupráce s dodavateli** je zaměřen na dodavatele, kteří nemají integraci výměny elektronických data (EDI) s aplikací Microsoft Dynamics 365 Supply Chain Management. To umožňuje dodavatelům práci s nákupními objednávkami, fakturami, informace o zásobách dodávek a požadavky na nabídku a také jim dává možnost mít přístup k části jejich dodavatelských hlavních dat. Tento článek vysvětluje, jak můžete spolupracovat s externími dodavateli, kteří používají rozhraní dodavatelské spolupráce k práci s nákupními objednávkami, požadavky na nabídku a zásobami dodávek. Také vysvětluje, jak konkrétnímu dodavateli umožnit používání dodavatelské spolupráce a definovat informace, které dodavatelé uvidí při odpovídání na nákupní objednávku.

Další informace o tom, co mohou externí dodavatelé provádět v rozhraní spolupráce dodavatelů, uvádí téma [Spolupráce dodavatelů s odběrateli](vendor-collaboration-work-customers-dynamics-365-operations.md).

Další informace o tom, jak mohou dodavatelé používat spolupráci s dodavateli v procesech fakturace, uvádí téma [Pracovní prostor fakturace dodavatelské spolupráce](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). Informace o zřizování nových uživatelů pro spolupráci s dodavateli uvádí téma [Správa uživatelů dodavatelské spolupráce](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Definování informací zobrazených dodavatelům při odpovědi na nákupní objednávky

Když dodavatelé reagují na nákupní objednávku, kterou jim pošlete, zobrazí se jedno ze tří oken se zprávou, ve kterém musí potvrdit, zda objednávku přijmou, odmítnou nebo přijmou se změnami. Vzhledem k tomu, že informace, které musí být zobrazeny v daném okamžiku dodavateli, můžou být specifické pro vaši firmu, můžete určit text, který se zobrazí v každé potvrzovací zprávě. Text například může informovat dodavatele o dalších krocích v procesu nebo podmínkách a ujednáních.

Chcete-li určit text, který se zobrazí v reakci na nákupní objednávky, postupujte podle těchto kroků

1. Na stránce **Informace pro dodavatele reagující na nákupní objednávky** vyberte typ reakce a pak vyberte **Upravit**.
2. V okně **Informační zpráva** zadejte informace, které mají být zobrazeny dodavatelům v okně se zprávou.

Pokud musíte přidat zprávy ve více jazycích, vytvořte samostatné zprávy a určete příslušný jazykový kód pro každou zprávu. Zpráva, která se každému dodavateli zobrazí, bude v jazyce, který používá.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Nastavení možností spolupráce pro konkrétního dodavatele

Správce konfiguruje obecná nastavení pro dodavatelskou spolupráci, jako jsou například role zabezpečení, které jsou k dispozici pro všechny dodavatele, se kterými spolupracujete. Existují však také nastavení, která se můžou lišit pro každý účet dodavatele. Tato nastavení byste měli nakonfigurovat.

- Povolte spolupráci s dodavatelem.
- Určete, zda má dodavatel vidět informace o ceně.

### <a name="enabling-vendor-collaboration"></a>Povolení spolupráce s dodavatelem

Před vytvořením uživatelských účtů pro externí dodavatele nakonfigurujte účet dodavatele, aby mohl dodavatel používat dodavatelskou spolupráci. Na stránce **Dodavatelé** na kartě **Obecné** nastavte pole **Aktivace spolupráce**. Existují tyto možnosti:

- **Aktivní (nákupní objednávka je automaticky potvrzena)**– nákupní objednávky se automaticky potvrzují, pokud je dodavatel přijme beze změn. Pokud použijete tuto možnost, nezapomeňte naplánovat dávkovou úlohu *Potvrdit přijaté nákupní objednávky z dodavatelské spolupráce*, která zodpovídá za zpracování potvrzení. Pokyny naleznete v další části.
- **Aktivní (nákupní objednávka není automaticky potvrzena)**– nákupní objednávky musí být ručně potvrzeny vaší organizací poté, co je dodavatel přijal.

### <a name="scheduling-the-auto-confirmation-batch-job"></a>Plánování dávkové úlohy automatického potvrzení

Pokud použijete možnost **Aktivní (PO je automaticky potvrzeno)** pro jednoho nebo více vašich dodavatelů (jak je popsáno v předchozí části), musíte naplánovat dávkovou úlohu *Potvrdit přijaté nákupní objednávky z dodavatelské spolupráce*, která je zodpovědná za zpracování a potvrzení vašich OP. Jinak k automatickému potvrzení nikdy nedojde. Úlohu můžete naplánovat následujícím postupem.

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Potvrzení nákupní objednávky \> Potvrdit přijaté nákupní objednávky z dodavatelské spolupráce**.
1. V dialogovém okně **Potvrdit přijaté nákupní objednávky z dodavatelské spolupráce** na pevné záložce **Spustit na pozadí** vyberte **Opakování**.
1. V dialogovém okně **Definujte opakování** definujte plán, podle kterého má úloha běžet. Při výběru plánu zvažte následující problémy:

    - Pokud váš systém zpracovává velký objem dat a spouští mnoho dávkových úloh, může být problém s výkonem. V tomto případě byste pravděpodobně neměli spouštět tuto úlohu častěji než každých 10 minut (v závislosti na vašich dalších požadavcích). Pokud pro vás výkon není problémem, můžete jej v případě potřeby spouštět tak často, jako každou 1 až 2 minuty.
    - Pokud mají vaši prodejci tendenci dodávat zboží rychle (v rámci dne, se kterým souhlasili), mělo by to být časté (asi každých 10 až 30 minut). Skladníci tak budou moci po potvrzení přijmout zboží oproti potvrzené nákupní objednávce.
    - Pokud mají vaši dodavatelé tendenci mít dlouhou dobu realizace (více než 24 hodin), můžete tuto úlohu nastavit tak, aby se spouštěla jen jednou denně nebo tak nějak.

1. Vyberte **OK**, chcete-li použít svůj plán a vrátit se do dialogového okna **Potvrdit přijaté nákupní objednávky z dodavatelské spolupráce**.
1. Podle potřeby nastavte další možnosti pozadí. Dialogové okno poskytuje obvyklé možnosti pro nastavení dávkových úloh v Supply Chain Management.

Další informace o dávkových úlohách viz [Přehled dávkového zpracování](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Určení, zda má dodavatel vidět informace o ceně

Pokud chcete sdílet informace o ceně pro nákupní objednávky prostřednictvím rozhraní dodavatelské spolupráce, je nutné nastavit možnost **Ceny/částky nákupní objednávky** na kartě **Výchozí nastavení nákupní objednávky** pro účet dodavatele na **Ano**. Tato Informace o ceně zahrnuje jednotkové ceny, slevy a poplatky.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Práce s nákupními objednávkami při použití dodavatelské spolupráce

### <a name="sending-a-po-to-a-vendor"></a>Odeslání nákupní objednávky dodavateli

Nákupní objednávky se připravují v Supply Chain Management. Pokud nákupní objednávka bude mít stav **Schváleno**, odesíláte ji dodavateli zvolením možnosti **Odeslat potvrzení** na stránce **Nákupní objednávka**. Stav nákupní objednávky se změní na **V externí revizi**. Po odeslání nákupní objednávky ji dodavatel může zobrazit na stránce **Nákupní objednávky ke kontrole** v rozhraní spolupráce dodavatele. Dodavatel pak může nákupní objednávku přijmout, odmítnout nebo pro ni navrhnout změny. Dodavatel může také přidat komentáře pro předávání informací, jako jsou například změny v nákupní objednávce. Pokud chcete tohoto dodavatele upozornit na novou nákupní objednávku, můžete také nákupní objednávky odeslat e-mailem pomocí systému správy tisku.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Potvrzení a přijetí nákupní objednávky dodavatelem

Poté, co dodavatel akceptuje nákupní objednávku, ta může být automaticky potvrzena nebo ji může být třeba potvrdit ručně. Toto chování závisí na tom, zda je hodnota v poli **Aktivace spolupráce** nastavena na **Aktivní (nákupní objednávka je automaticky potvrzena)** nebo na **Aktivní (nákupní objednávka není automaticky potvrzena)** pro dodavatele.

Následující tabulka zobrazuje typické výměny informací v závislosti na odpovědi dodavatele, když mu je odeslána objednávky k potvrzení:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Odpověď dodavatele</th>
<th>Výsledek</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Dodavatel <strong>přijímá</strong> objednávku a aplikace Supply Chain Management je nakonfigurována tak, aby automaticky potvrdila nákupní objednávky, které dodavatel přijme.</td>
<td>Stav objednávky bude aktualizován na hodnotu <strong>Potvrzeno</strong>. Pokud nelze z nějakého důvodu objednávku aktualizovat, odpověď dodavatele i tak bude zaznamenána jako<strong> Přijato</strong>, ale nákupní objednávka zůstane ve stavu <strong>Externí revize</strong>. 

Nákupní objednávka, která byla odeslána dodavateli a má stav <strong>Externí revize</strong>, se aktualizuje s potvrzenými daty dodání na řádcích. Tato aktualizace zahájí novou verzi, která bude automaticky nastavena na stav <strong>potvrzeno</strong>. Potvrzená nákupní objednávka se zobrazí v rozhraní dodavatelské spolupráce.</td>
</tr>
<tr class="odd">
<td>Dodavatel <strong>přijímá</strong> objednávku, ale aplikace Supply Chain Management není nakonfigurována tak, aby automaticky potvrdila nákupní objednávky, které dodavatel přijme.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Přijato</strong>, ale nákupní objednávka zůstane ve stavu <strong>Na externí kontrole</strong>.

Nákupní objednávka, která byla odeslána dodavateli a má stav <strong>Externí revize</strong>, se aktualizuje s potvrzenými daty dodání na řádcích. Tato aktualizace zahájí novou verzi, která bude automaticky nastavena na stav <strong>V externí revizi</strong>. Poté lze ručně potvrdit nákupní objednávku.</td>
</tr>
<tr class="even">
<td>Dodavatel <strong>odmítne</strong> objednávku.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Zamítnuto</strong> a nákupní objednávka zůstane ve stavu <strong>Na externí kontrole</strong>. Odmítnutí je přijato společně s poznámkou pro dodavatele.</td>
</tr>
<tr class="odd">
<td>Dodavatel <strong>přijme</strong> objednávku <strong>se změnami</strong>. Na úrovni řádků je možné navrhnout změny. Dodavatele může přijmout nebo odmítnout jednotlivé řádky. Zde jsou některé další změny, které může dodavatel navrhnout:
<ul>
<li>Změna dat nebo množství.</li>
<li>Rozdělení řádků pro jiná data dodání nebo množství.</li>
<li>Náhrada zboží.</li>
</ul>
Údaje o ceně a náklady nemůže změnit dodavatel. Dodavatel však může navrhnout tyto změny pomocí poznámek.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Přijato se změnami</strong> a stav nákupní objednávky zůstane <strong>Na externí kontrole</strong>. Stavy zobrazují typy změn, které navrhl dodavatel. Informace týkající se automatické spotřeby změn naleznete níže v tomto článku v části &quot;Aktualizace nákupní objednávky, když dodavatel navrhne změny&quot;. </td>
</tr>
</tbody>
</table>

Pomocí pracovního prostoru **Příprava nákupní objednávky** můžete sledovat, na které nákupní objednávky dodavatel zareagoval. Tento pracovní prostor obsahuje dva seznamy s nákupními objednávkami se stavem **V externí revizi**:

- Na externí kontrole – vyžaduje akci
- Na externí kontrole čekající na odpověď dodavatele

### <a name="changing-a-po"></a>Změna objednávky

Pokud chcete změnit nákupní objednávku, na kterou dodavatel reagoval, musíte odeslat dodavateli novou verzi nákupní objednávky. Nová nákupní objednávka bude mít příponu, která značí, že se jedná o upravenou verzi nákupní objednávky, která byla dříve odeslána. Stránka **Historie potvrzení nákupních objednávek dodavatele** umožnuje sledování historie každé objednávky. Dříve potvrzené verze nákupní objednávky zůstane v seznamu potvrzených nákupních objednávek, dokud není potvrzena nová nákupní objednávka.

### <a name="canceling-a-po"></a>Zrušení nákupní objednávky

Při zrušení objednávky je stav změněn na **Schváleno**. Je nutné odeslat nákupní objednávku zpět dodavateli, aby dodavatel mohl potvrdit nebo zamítnout zrušení. Po potvrzení zrušení se nákupní objednávka zobrazí v seznamu potvrzených nákupních objednávek jako **Zrušeno**.

### <a name="adding-attachments-to-a-po"></a>Přidání přílohy k nákupní objednávce

Do nákupní objednávky můžete přidávat přílohy, například soubory obrázků a poznámky, pomocí systému správy dokumentů. Přílohy typu **Externí** dodavatel uvidí až poté, co mu pošlete nákupní objednávku.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Aktualizace nákupní objednávky, když dodavatel navrhne změny

Když dodavatel odpoví na nákupní objednávku a navrhne změny, je dalším krokem zpracování odpovědi.

V pracovním prostoru **Příprava nákupní objednávky** v seznamu **Na externí kontrole - vyžaduje akci**, můžete identifikovat nákupní objednávku, kterou dodavatel přijal se změnami. Z tohoto seznamu můžete také přejít na odpověď dodavatele.

Při odpovědi dodavatel může změnit následující informace v záhlaví:
 
- Odkaz na dokument dodavatele
- Způsob dodání
- Dodací podmínky
- Potvrzené datum dodání

Dodavatel může také přidat poznámku nebo přílohu.

Na řádcích dodavatele lze změnit množství a data dodání, přidávat poznámky a přílohy, zamítnout řádek, nahradit řádek jiným produktem, který je zadaný jako text, a rozdělit řádek na více dodávek. Stav řádku se liší podle změny, které navrhl dodavatel:
    
- **Přijato se změnami**
- **Odmítnuto**
- **Nahrazeno** – V tomto případě bude přidán další řádek, který má stav **Náhrada**.
- **Potvrzeno**
- **Rozdělit na plán** – v tomto případě budou přidány extra řádky se stavem **Naplánovat řádky**.

Pokud řádek nemá žádné změny, stav řádku bude **Přijato**.

Při odpovědi vám stavy řádku řeknou typy změn provedené dodavatelem. Kromě toho se všechna změněná pole se zobrazí tučně, což usnadňuje identifikaci změn.

Objednávky lze aktualizovat volbou akce **Zpracovat aktualizaci PO** v odpovědi nebo v jednom řádku po druhém. Pole **Je zpracována aktualizace nákupní objednávky?** v záhlaví a řádky označují, zda systém zpracoval záhlaví nebo řádky k aktualizaci nákupní objednávky se změnami, které pocházejí z odpovědi. Akci **Zpracovat aktualizaci PO** můžete spustit pouze jednou na záhlaví nebo řádek.

Ne všechny navrhované změny lze na nákupní objednávce aktualizovat. Pouze aktualizace v záhlaví a aktualizace dat a množství na řádcích lze automaticky aktualizovat v nákupní objednávce. Další změny musíte aktualizovat ručně na nákupní objednávce. V takovém případě hodnota pole **Je PO zpracována?** je **Ruční aktualizace**. Například pokud dodavatel navrhne, že řádek lze rozdělit na plán, tuto změnu je nutné provést ručně.

Všechny řádky, které se nachází ve stavu **Přijato**, budou mít potvrzené datum dodání. Při spuštění akce **Zpracovat aktualizaci nákupní objednávky** se toto datum aktualizuje na nákupní objednávce. Poznámky a přílohy nejsou automaticky převedeny na aktuální nákupní objednávku. Všimněte si, že když aktualizujete aktuální nákupní objednávku prostřednictvím akce **Zpracovat aktualizaci nákupní objednávky**, akce obchodu nebudou na řádcích nákupní objednávky znovu posuzovány.

## <a name="po-statuses-and-versions"></a>Stavy a verze nákupní objednávky

V této části jsou popsány různé stavy, které může mít nákupní objednávky až do doby, než je potvrzena. Popisuje také, kdy jsou nové verze nákupní objednávky dostupné pro dodavatele. Chování se liší v závislosti na tom, zda používáte správu změn pro nákupní objednávky. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Verze a stavy, jestliže nepoužíváte správu změn

Následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít.

| Akce | Stav a verze |
|--------|--------------------|
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Supply Chain Management. | Stav je **Schváleno**. |
| Nákupní objednávka je odeslána dodavateli. | Verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**. |
| Dodavatel odešle odpověď **Přijata se změnami**. | Stav bude stále **Na externí kontrole**. |
| Provedete změny, které jsou požadovány dodavatelem. | Stav je změněn na **Schváleno**. |
| Odešlete novou verzi nákupní objednávky dodavateli. | Nová verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**. |
| Dodavatel přijme novou verzi nákupní objednávky. | Stav bude stále **V externí revizi**, pokud není nakonfigurován účet dodavatele na nákupní objednávce na automatické nastavení stavu na **Potvrzeno** při přijetí dodavatelem. |

Dodavatelé nemusí nákupní objednávku potvrdit pomocí rozhraní spolupráce pro dodavatele. Mohou také odeslat e-mailovou zprávu nebo sdělit jejich přijetí nákupní objednávky prostřednictvím jiných kanálů. Poté lze ručně potvrdit objednávku. V tomto případě se zobrazí upozornění, že objednávka má být potvrzena, přestože není reakce od dodavatele. Nákupní objednávka se poté zobrazí v historii potvrzení jako otevřená potvrzená objednávka, která nemá žádné odpovědi. V tomto okamžiku dodavatel již nemá možnost nákupní objednávku potvrdit nebo odmítnout.

> [!NOTE]
> Poznámka: verze nákupní objednávky, která je dostupná pro jiné procesy v aplikaci Supply Chain Management, je vždy nejnovější verze, a to i v případě, že tato nebyla registrována v rozhraní pro spolupráci dodavatele.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Verze a stavy, jestliže používáte správu změn

Pokud povolíte správu změn pro nákupní objednávky, nákupní objednávky procházejí workflowem schválení, aby získaly stav **Schváleno**. Tento proces dodavateli není viditelný.

Pokud je povolena Správa změn, následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít. Verze je registrována po schválení nákupní objednávky, nikoliv když je nákupní objednávka odeslána dodavateli nebo potvrzena.

| Akce | Stav a verze |
|--------|--------------------|
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Supply Chain Management. | Stav majetku je **Koncept**. |
| Nákupní objednávka je odeslána do schvalovacího procesu. (Schvalovací proces je interním procesem, do kterého dodavatel nevstupuje.) | Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávky není během procesu schvalování zamítnuta. Schválená nákupní objednávka je registrována jako verze. | 
| Nákupní objednávka je odeslána dodavateli. | Verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**. |
| Provedete některé změny požadované dodavatelem, ať už manuálně nebo použitím akce **Zpracovat aktualizaci nákupní objednávky** v odpovědi na aktualizaci nákupní objednávky. | Stav je opět změněn na **Koncept**. |
| Nákupní objednávka je opět odeslána do schvalovacího procesu. | Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávky není během procesu schvalování zamítnuta. Alternativně systém lze nakonfigurovat tak, aby změny konkrétního pole nevyžadovaly opětovné schválení. V tomto případě se stav nejprve změní na **Koncept**, a pak se automaticky aktualizuje na **Schváleno**. Schválená nákupní objednávka je registrována jako nová verze. |
| Odešlete novou verzi nákupní objednávky dodavateli. | Nová verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**. |
| Dodavatel schválí novou verzi nákupní objednávky. | Stav se změní na **Potvrzeno** buď automaticky nebo když obdržíte odpověď od dodavatele a poté potvrdíte nákupní objednávku. |

## <a name="sharing-information-about-consignment-inventory"></a>Sdílení informací o zásobách dodávky

Pokud používáte zásoby dodávky, dodavatelé mohou použít rozhraní spolupráce dodavatele k zobrazení informací na následujících stránkách:

- **Nákupní objednávky spotřebovávající zásoby dodávek** – Nákupní objednávky pro zásoby dodávek jsou generovány při změně vlastnictví zásob od dodavatele pro vaši společnost. Současně dojde k zaúčtování příjemky produktu. Tyto nákupní objednávky dodávek se zobrazí pouze na stránce **Nákupní objednávky spotřebovávající zásoby dodávek**. Nejsou zahrnuty na stránce **Všechny potvrzené nákupní objednávky** v modulu **Dodavatelská spolupráce**.
- **Přijaté produkty ze zásob dodávky** – Tato stránka uvádí seznam všech transakcí, kde bylo vlastnictví produktů převedeno z dodavatele na vaši společnost. Tyto informace mohou dodavatelé použít k fakturaci zákazníkovi.
- **Zásoby dodávky na skladě** - Tato stránka zobrazuje zásoby dodávky na skladě vlastněné dodavatelem, které jsou k dispozici ve vašem skladu.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Práce s požadavky na nabídku při použití dodavatelské spolupráce

Tato část popisuje interakce mezi odběrateli a dodavateli při zpracování požadavku na nabídku. Také vysvětluje, jak jsou informace komunikovány dodavatelům. Základní přehled podpory pro zpracování požadavku na nabídku naleznete v tématu [Přehled požadavků na nabídku (RFQ)](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternativy, přílohy, dodatky a vrácení

- **Alternativy** – na hlavičce případu požadavku na nabídku můžete určit, že alternativy jsou povoleny pro nekatalogové řádky položky. Pokud jsou povoleny alternativy, dodavatele mohou přidat řádek alternativy pro každý požadovaný řádek.
- **Přílohy** – přílohy lze přidat na úrovni záhlaví i na úrovni řádku případu požadavku na nabídku. Přílohy lze klasifikovat jako interní nebo externí. Interní přílohy lze zobrazit pouze na straně odběratele, zatímco dodavatelé mohou zobrazit externí přílohy po jejich odeslání.

    Dodavatelé mohou také přidat přílohy ve své odpovědi na nabídku. Tyto přílohy lze zobrazit na straně odběratele poté, co dodavatel odešle odpovědi na nabídku. Přílohy, které dodavatelé přidají, jsou vždy klasifikovány jako externí. Abyste získali přístup k příloze, kterou dodavatel odeslal spolu nabídkou, zvolte **Přílohy nabídky** nebo **Přílohy řádku nabídky**.
    
    K otevření příloh, které byly odeslány společně s případem požadavku na nabídku, použijte symbol kancelářské sponky na odpovědi.

- **Dodatky** – po dokončení dodatku jsou existující odpovědi na nabídku odstraněny, aby mohly být nahrazeny aktualizovanými hodnotami. Informace o řádkové ceně a množství z předchozích odpovědí na nabídku lze zobrazit pomocí deníků na případu požadavku na nabídku.

    K vynucení zpracování dodatku na stránce **Parametry modulu Zásobování a zdroje** na pevné záložce **Požadavek na nabídky** nastavte možnost **Zamknout požadavky na nabídku při jejich odeslání** na **Ano**. (Tato možnost je nastavena a požadovaná pro veřejný sektor)

- **Vrácení** – pokud dodavatel předložil nabídku, ale další nebo změněné informace jsou vyžadovány pro případ požadavku na nabídku, odběratel může vrátit nabídka dodavateli. Data z nabídky, která byla dříve odeslaná, se zachovají, a dodavatel může provést požadované úpravy, aniž by bylo nutné znovu spustit proces nabídky.

## <a name="public-sector-extensions"></a>Rozšíření veřejného sektoru

Pro veřejný sektor rozšířená funkce umožňuje odeslání případu požadavku na nabídku dodavatelům a jeho publikování. Když publikujete požadavek na nabídku, kdokoliv kdo požádá o informace, může zobrazit práci, která je v souladu s předpisy z veřejného sektoru. Všechny dostupné práce se promítnou na stránce se seznamem **Otevřené publikované požadavky na nabídky** a zrušené, čekající nebo přidělené požadavky na nabídku lze zobrazit na stránce se seznamem **Uzavřené publikované požadavky na nabídky** stránku se seznamem. Tyto dokumenty lze zobrazit také na webu mimo aplikaci Supply Chain Management pomocí integrací s následujícími datovými entitami:

- Publikované požadavky na nabídky
- Řádek publikovaných požadavků na nabídky
- Přílohy záhlaví publikovaných požadavků na nabídky

Tyto entity umožnují lidem, kteří nejsou zřízení uživatelé v aplikaci Supply Chain Management, ale mají anonymní přístup k externímu webu, zobrazovat dostupnou a uzavřenou práci. Kromě toho rozšířená funkce v **Odeslat a publikovat** poskytuje uživateli, který nastavuje parametry pro proces požadavku na nabídku, definovat šablonu e-mailu. Když pak pracovník zásobování vytvoří případ požadavku na nabídku, musí zvolit šablonu e-mailu pro odeslání požadovaných informací dodavatelům ohledně případu požadavku na nabídku. 

Uživatel, který nastavuje parametry pro proces požadavku na nabídku, může vytvořit více šablon e-mailu. Tyto e-mailové šablony mohou obsahovat statický text i následující tokeny nahrazení. Tokeny budou nahrazeny kontextovými hodnotami při vytvoření e-mailu.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Pokud je požadován dodatek a je odeslán po odeslání požadavku na nabídku, požadavek na nabídku bude odeslán znovu všem pozvaným dodavatelům. Publikovaný dokument bude také aktualizován na stránce **Otevřené publikované požadavky na nabídky**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
