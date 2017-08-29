---
title: "Spolupráce dodavatelů s externími dodavateli"
description: "Toto téma vysvětluje, jak nákupčí mohou spolupracovat s externími dodavateli na výměně informací o nákupních žádankách a zásobách dodávky."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: cbd099403f48b502ca74bcb38ae12decedb8f2da
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>Spolupráce dodavatelů s externími dodavateli

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak nákupčí mohou spolupracovat s externími dodavateli na výměně informací o nákupních žádankách a zásobách dodávky.

Modul **Spolupráce s dodavateli** je zaměřen na dodavatele, kteří nemají integraci výměny elektronických data (EDI) s aplikací Microsoft Dynamics 365 for Finance and Operations. Umožňuje dodavatelům pracovat s informacemi z nákupní objednávky, faktury a dodávky zásob. Toto téma popisuje, jak spolupracovat externího dodavatele, kteří jsou použití rozhraní spolupráce dodavatele při práci s POs a zásilka zásob. Také uvádí, jak konkrétnímu dodavateli umožnit používání spolupráce dodavatele a definovat informace, které dodavatelé uvidí při odpovídání na NO. Další informace o tom, co mohou externí dodavatelé provádět v rozhraní spolupráce dodavatelů, uvádí téma [Spolupráce dodavatelů s odběrateli](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Další informace o tom, jak mohou dodavatelé používat spolupráci s dodavateli v procesech fakturace, uvádí téma [Pracovní prostor fakturace dodavatelské spolupráce](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Informace o zřizování nových uživatelů pro spolupráci s dodavateli uvádí téma [Správa uživatelů dodavatelské spolupráce](manage-vendor-collaboration-users.md).

Další informace o tom, jak mohou dodavatelé používat spolupráci s dodavateli v procesech fakturace, uvádí téma [Pracovní prostor fakturace dodavatelské spolupráce](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). 

Informace o zřizování nových uživatelů pro spolupráci s dodavateli uvádí téma [Správa uživatelů dodavatelské spolupráce](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Definování informací zobrazených dodavatelům při reagování na nákupní objednávky
Když dodavatelé reagují na nákupní objednávku, kterou jim pošlete, zobrazí se dialogové okno, ve kterém musí potvrdit, zda objednávku přijmou, odmítnou nebo přijmou se změnami. Vzhledem k tomu, že informace, které musí být zobrazeny v daném okamžiku dodavateli, můžou být specifické pro vaši firmu, můžete určit text, který se zobrazí ve všech třech potvrzovacích zprávách. Text například může informovat dodavatele o dalších krocích v procesu nebo podmínkách a ujednáních.  

Chcete-li určit text, který se zobrazí v reakci na nákupní objednávky:

1.  Otevřete stránku **Informace pro dodavatele reagující na nákupní objednávky**.
2.  Vyberte jeden z typů odpovědí.
3.  Klikněte na možnost **Upravit**.
4.  Zadejte informace, které se mají dodavatelům zobrazit v poli **informační zpráva**.

Pokud musíte přidat zprávy ve více jazycích, vytvořte samostatné zprávy a určete příslušné jazykové kódy. Zpráva, která se dodavateli zobrazí, bude v jazyce, který používá.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Nastavení možností spolupráce pro konkrétního dodavatele
Obecné nastavení spolupráce dodavatele v aplikaci Finance and Operations konfiguruje správce. Správce například určí role zabezpečení, které jsou k dispozici pro všechny dodavatele, s nimiž spolupracujete. Existují také nastavení, která se můžou lišit pro každý účet dodavatele a měli byste je nastavit:
-   Povolte spolupráci s dodavatelem.
-   Rozhodněte, zda dodavatele může zobrazit informace o ceně.

### <a name="enable-vendor-collaboration"></a>Povolení spolupráce s dodavatelem.

Před vytvořením uživatelských účtů pro externí dodavatele nakonfigurujte účet dodavatele, aby mohli používat spolupráce dodavatele. Chcete-li to provést, nastavte pole **Aktivace spolupráce** na aktivní na kartě **Obecné** na stránce **Dodavatelé**. Existují dvě možnosti, které je možné vybrat:

-   **Aktivní (nákupní objednávky je automaticky potvrzena)**– nákupní objednávky se automaticky potvrzují poté, co je dodavatel přijme beze změn.
-   **Aktivní (nákupní objednávka není automaticky potvrzená)**-nákupní objednávky musí být ručně potvrzeny ve vaší organizaci poté, co je dodavatel přijal.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Rozhodnutí, zda dodavatele může zobrazit informace o ceně

Pokud chcete dodavateli sdělit informace o cenách, jako je jednotková cena, slevy a poplatky, přes rozhraní pro spolupráci, je nutné nastavit možnost **Ceny/částky nákupní objednávky** v účtu dodavatele na **Ano**. Tato možnost je k dispozici na kartě **Výchozí nastavení nákupní objednávky**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Práce s nákupními objednávkami při použití spolupráce dodavatele
### <a name="sending-a-po-to-the-vendor"></a>Odeslání nákupní objednávky dodavateli

Nákupní objednávky jsou připraveny v modulu Finance and Operations. Pokud nákupní objednávka bude mít stav **Schváleno**, odesíláte ji dodavateli pomocí akce **Odeslat potvrzení** na stránkce **Nákupní objednávka**. Stav nákupní objednávky se změní na **V externí revizi**. Po odeslání nákupní objednávky ji dodavatel může zobrazit na stránce **Nákupní objednávky ke kontrole** v rozhraní spolupráce dodavatele. Dodavatel pak může objednávku přijmout, odmítnout nebo pro ni navrhnout změny. Dodavatel může také přidat komentáře pro předávání informací, jako jsou například změny v nákupní objednávce. Pokud chcete tohoto dodavatele upozornit na novou nákupní objednávku, můžete také nákupní objednávky odeslat e-mailem pomocí systému správy tisku.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Potvrzení a přijetí nákupní objednávky dodavatelem

Když dodavatel potvrdí nákupní objednávku, může být nákupní objednávka automaticky potvrzena nebo může být nutné ji potvrdit ručně. Toto chování závisí na tom, zda je hodnota v poli **Aktivace dodavatele** nastavena na **Aktivní (nákupní objednávka je automaticky potvrzena)** nebo na **Aktivní (nákupní objednávka není automaticky potvrzena)** pro dodavatele.  

Následující tabulka zobrazuje typické výměny informací v závislosti na odpovědi dodavatele, když mu je odeslána objednávky k potvrzení:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Odpověď dodavatele</strong></td>
<td><strong>Výsledek</strong></td>
</tr>
<tr class="even">
<td>Dodavatel <strong>přijme</strong> objednávku. Aplikace Finance and Operations není nakonfigurována na automatické potvrzení nákupních objednávek, když je dodavatel přijme.</td>

<td>Stav objednávky bude aktualizován na hodnotu <strong>Potvrzeno</strong>. Pokud něco brání aktualizaci objednávky, odpověď dodavatele i tak bude zaznamenána jako <strong>Přijato</strong>, ale nákupní objednávka zůstane ve stavu <strong>Externí revize</strong>. 

Nákupní objednávka, která byla odeslána dodavateli a má stav **Externí revize**, se aktualizuje s potvrzenými daty dodání na řádcích. Aktualizace zahájí novou verzi, která bude automaticky aktualizována na stav **potvrzeno**. Potvrzená nákupní objednávka se zobrazí v rozhraní spolupráce dodavatele.</td>
</tr>
<tr class="odd">
<td>Dodavatel <strong>přijme</strong> objednávku. Aplikace Finance and Operations není nakonfigurována na automatické potvrzení nákupních objednávek, když je dodavatel přijme.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Přijato</strong>, ale nákupní objednávka zůstane ve stavu <strong>Na externí kontrole</strong>.

Nákupní objednávka, která byla odeslána dodavateli a má stav **Externí revize**, se aktualizuje s potvrzenými daty dodání na řádcích. Aktualizace zahájí novou verzi, která bude nastavena na stav **V externí revizi**. Pak budete moci ručně potvrdit nákupní objednávku.</td>

</tr>
<tr class="even">
<td>Dodavatel <strong>odmítne</strong> objednávku.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Zamítnuto</strong> a nákupní objednávka zůstane ve stavu <strong>Na externí kontrole</strong>. Odmítnutí je přijato společně s poznámkou dodavatele.</td>
</tr>
<tr class="odd">
<td>Dodavatel <strong>přijme objednávku se změnami</strong>. Na úrovni řádků je možné navrhnout změny. Je možné přijmout nebo odmítnout jednotlivé řádky. Další možné změny zahrnují:
<ul>
<li>Změna dat nebo množství.</li>
<li>Rozdělení řádků pro jiná data dodání nebo množství.</li>
<li>Nahrazení zboží.</li>
</ul>
Údaje o ceně a náklady nemůže změnit dodavatel. Návrhy na tyto změny mohou být provedeny pomocí poznámek.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Přijato se změnami</strong> a stav nákupní objednávky zůstane <strong>Na externí kontrole</strong>. Stavy zobrazují typy změn, které navrhl dodavatel. Informace týkající se automatické spotřeby změn naleznete v části dole, která se týká postupu při aktualizaci, když dodavatel navrhne změny. </td>
</tr>
</tbody>
</table>

Pomocí pracovního prostoru **Příprava** **nákupní objednávky** můžete sledovat, na které nákupní objednávky dodavatel zareagoval. Tento pracovní prostor obsahuje dva seznamy s nákupními objednávkami se stavem **Na externí kontrole**:

-   Na externí kontrole – vyžaduje akci.
-   Na externí kontrole čekající na odpověď dodavatele.

### <a name="changing-a-po"></a>Změna objednávky

Pokud chcete změnit nákupní objednávku, na kterou dodavatel reagoval, musíte odeslat dodavateli prostřednictvím portálu novou verzi nákupní objednávky. Nová nákupní objednávka bude mít příponu, která značí, že se jedná o upravenou verzi nákupní objednávky té, která byla dříve předána. Stránka **Historie potvrzení nákupních objednávek dodavatele** umožnuje sledování historie každé objednávky. Dříve potvrzené verze nákupní objednávky zůstane v seznamu potvrzených nákupních objednávek, dokud není potvrzena nová nákupní objednávka.

### <a name="cancelling-a-po"></a>Zrušení nákupní objednávky

Při zrušení objednávky je stav změněn na **Schváleno**. Je nutné odeslat nákupní objednávku zpět dodavateli prostřednictvím portálu pro dodavatele, aby dodavatel mohl dodavatel potvrdit nebo zamítnout zrušení. Po potvrzení zrušení se nákupní objednávka zobrazí v seznamu potvrzených nákupních objednávek jako **Zrušeno**.

### <a name="adding-attachments-to-a-po"></a>Přidání přílohy k nákupní objednávce

Do nákupní objednávky můžete přidávat přílohy, například soubory obrázků a poznámky, pomocí systému správy dokumentů. Přílohy typu **Externí** dodavatel uvidí až poté, co mu pošlete nákupní objednávku.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Aktualizace nákupní objednávky, když dodavatel navrhne změny
Když dodavatel odpoví na nákupní objednávku a navrhne změny, je dalším krokem zpracování odpovědi.
V **pracovním prostoru Příprava nákupní objednávky** v seznamu akcí potřebných pro externí revizi můžete identifikovat nákupní objednávku, na kterou dodavatel reagoval, jako přijatou se změnami. V seznamu akcí potřebných pro externí revizi můžete také přejít na odpověď dodavatele. Dodavatel může reagovat tak, že změní následující informace v záhlaví.
 
-   Odkaz na dokument dodavatele
-   Způsob dodání
-   Dodací podmínky
-   Potvrzené datum dodání

Dodavatel může také přidat poznámku nebo přílohu

Na řádcích dodavatele lze změnit množství a data dodání, přidávat poznámky a přílohy, zamítnout řádek, nahradit řádek jiným produktem, který je zadaný jako text, a rozdělit řádek na více dodávek. V závislosti na tom, jaké změny dodavatel navrhuje, bude mít stav řádku různé stavy:
    
-   **Přijato se změnami**
-   **Odmítnuto**
-   **Nahrazeno** – V tomto případě bude přidán další řádek, který má stav **náhradní**.
-   **Potvrzeno** rozdělení do plánu – v tomto případě budou přidány extra řádky se stavem **Naplánovat řádky**.

Pokud řádek nemá žádné změny, stav řádku bude **Přijato**.

Můžete reagovat tak, že zobrazíte dříve uvedené stavy řádků, které označují typy změn provedených dodavatelem. Kromě toho se budou všechna změněná pole zobrazovat tučně, což usnadňuje identifikaci změn.

Objednávky lze aktualizovat klepnutím na akci **Zpracovat aktualizaci PO** v odpovědi nebo v jednom řádku po druhém. Indikátor **Je zpracována aktualizace nákupní objednávky?** v záhlaví a řádky umožňují zobrazit, zda má systém zpracoval záhlaví nebo řádky k aktualizaci nákupní o jakékoli potenciální změny vzešlé z odpovědi. Proces **Zpracovat aktualizaci PO** můžete spustit pouze jednou na záhlaví nebo řádek.

Ne všechny navrhované změny lze na nákupní objednávce aktualizovat. Pouze aktualizace v záhlaví a aktualizace dat a množství na řádcích lze automaticky aktualizovat v nákupní objednávce. Další změny musíte aktualizovat ručně na nákupní objednávce. V takovém případě indikátor **Je PO zpracována?** zobrazuje **ruční aktualizace**. Příkladem změny, která má být zpracována ručně, by byl příklad, kdy dodavatele doporučí rozdělení řádku na plán.

Řádek, který má stav **přijaté**, bude mít potvrzené datum dodání,které bude aktualizováno na nákupní objednávce při provedení příkazu **Zpracovat aktualizaci PO**. Poznámky a přílohy nebudou automaticky převedeny na aktuální nákupní objednávku. Všimněte si, že když aktualizujete aktuální nákupní objednávku prostřednictvím akce **Zpracovat aktualizaci PO**, akce obchodu nebudou na řádcích nákupní objednávky znovu posuzovány.


## <a name="po-statuses-and-versions"></a>Stavy a verze nákupní objednávky
V této části jsou popsány různé stavy, které může mít nákupní objednávky až třikrát kdy byla potvrzena. Popisuje také, v jakém okamžiku jsou nové verze nákupní objednávky dostupné pro dodavatele. Chování se liší v závislosti na tom, zda používáte správu změn pro nákupní objednávky. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Verze a stavy, jestliže nepoužíváte správu změn

Následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Akce**                                                               | **Stav a verze**                                                                                                                                       |
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Finance and Operations. | Stav je **Schváleno**.                                                                                                                                  |
| Nákupní objednávka je odeslána dodavateli.                                            | Verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.                                          |
| Dodavatel odešle odpověď **Přijata se změnami**.                  | Stav bude stále **Na externí kontrole**.                                                                                                                  |
| Provedete změny, které jsou požadovány dodavatelem.                  | Stav je změněn na **Schváleno**.                                                                                                                        |
| Odešlete novou verzi nákupní objednávky dodavateli.                        | Nová verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.                                      |
| Dodavatel přijme novou verzi nákupní objednávky.                            | Stav bude stále **Na externí revizi**, pokud není nakonfigurován účet dodavatele na nákupní objednávce na automatické nastavení stavu na **Potvrzeno** při přijetí. |


Dodavatelé nemusí nákupní objednávku potvrdit pomocí rozhraní spolupráce pro dodavatele. Mohou také odeslat e-mailovou zprávu nebo sdělit jejich přijetí nákupní objednávky prostřednictvím jiných kanálů. Potvrďte objednávku ručně v aplikaci Finance and Operations. V tomto případě se zobrazí upozornění, že objednávka má být potvrzena, přestože není reakce od dodavatele. Nákupní objednávka se poté zobrazí v historii potvrzení jako otevřená potvrzená objednávka, která nemá žádné odpovědi. Dále dodavatel již nemá možnost nákupní objednávku potvrdit nebo odmítnout.  


>[!NOTE]
>Poznámka: verze nákupní objednávky, která je dostupná pro jiné procesy v aplikaci Dynamics 365 for Finance and Operations, je vždy nejnovější verze, a to i v případě, že tato nebyla registrována v rozhraní pro spolupráci dodavatele.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Verze a stavy, jestliže používáte správu změn

Pokud povolíte správu změn pro nákupní objednávky, nákupní objednávky procházejí workflowem schválení, aby získaly stav **Schváleno**. Tento proces dodavateli není viditelný.  

Pokud je povolena Správa změn, následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít. Verze je registrována po schválení nákupní objednávky, nikoliv když je nákupní objednávka odeslána dodavateli nebo potvrzena.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Akce**                                                               | **Stav a verze**                                                                                                                                       |
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Finance and Operations.      | Stav majetku je **Koncept**.  |
| Nákupní objednávka je odeslána do schvalovacího procesu. (Schvalovací proces je interním procesem, do kterého dodavatel nevstupuje.)                                                           | Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávka není během procesu schvalování zamítnuta. Schválená nákupní objednávka je registrována jako verze.           | 
| Nákupní objednávka je odeslána dodavateli.                                                            | Verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.      |
| Provedete změny požadované dodavatelem ať už manuálně nebo použitím akce v odpovědi na aktualizaci nákupní objednávky.                                                            | Stav je opět změněn na **Koncept**.     |
|Nákupní objednávka je opět odeslána do schvalovacího procesu.                                                |  Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávka není během procesu schvalování zamítnuta. Alternativně systém lze nakonfigurovat tak, aby změny konkrétního pole nevyžadovaly opětovné schválení. V tomto případě se stav nejprve změní na **Koncept**, a pak se automaticky aktualizuje na **Schváleno**. Schválená nákupní objednávka je registrována jako nová verze.                                         |
|Odešlete novou verzi nákupní objednávky dodavateli.                                                |  Nová verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.                                         |
|Dodavatel schválí novou verzi nákupní objednávky.                                                |  Stav se změní na **Potvrzeno** buď automaticky nebo když obdržíte odpověď od dodavatele a poté potvrdíte nákupní objednávku. |

## <a name="share-information-about-consignment-inventory"></a>Sdílení informací o zásobách
Pokud používáte zásoby na skladě, dodavatelé mohou použít rozhraní spolupráce dodavatele k zobrazení informací na následujících stránkách:

-   **Nákupní objednávky spotřebovávající zásoby dodávek** – nákupní objednávky pro zásoby dodávek jsou generovány při změně vlastnictví zásob od dodavatele pro vaši společnost. Současně dojde k zaúčtování příjemky produktu. Tyto nákupní objednávky se zobrazí pouze na stránce **Nákupní objednávky spotřebovávající zásoby dodávek**. Nejsou zahrnuty na stránce **Všechny potvrzené nákupní objednávky** v modulu **Dodavatelská spolupráce**.
-   **Přijaté produkty ze zásob dodávky** - Tato stránka uvádí seznam všech transakcí, kde bylo vlastnictví produktů převedeno z dodavatele na vaši společnost. Tyto informace mohou dodavatelé použít k fakturaci zákazníkovi.
-   **Zásoby dodávky na skladě** - tato stránka zobrazuje zásoby dodávky na skladě vlastněné dodavatelem, které jsou k dispozici ve vašem skladu.





