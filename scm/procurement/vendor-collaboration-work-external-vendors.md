---
title: "Spolupráce dodavatelů s externími dodavateli"
description: "Toto téma vysvětluje, jak nákupčí mohou spolupracovat s externími dodavateli na výměně informací o nákupních žádankách a zásobách dodávky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: d585ae0716a4bd9c3531e8639cd7c6b3cab780ac
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Spolupráce dodavatelů s externími dodavateli

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak nákupčí mohou spolupracovat s externími dodavateli na výměně informací o nákupních žádankách a zásobách dodávky.

Modul **Spolupráce s dodavateli** je zaměřen na dodavatele, kteří nemají integraci výměny elektronických data (EDI) s aplikací Microsoft Dynamics 365 for Operations. Umožňuje dodavatelům pracovat s informacemi z nákupní objednávky, faktury a dodávky zásob. Toto téma popisuje, jak spolupracovat externího dodavatele, kteří jsou použití rozhraní spolupráce dodavatele při práci s POs a zásilka zásob. Také uvádí, jak konkrétnímu dodavateli umožnit používání spolupráce dodavatele a definovat informace, které dodavatelé uvidí při odpovídání na NO. Další informace o tom, co mohou externí dodavatelé provádět v rozhraní spolupráce dodavatelů, uvádí téma [Spolupráce dodavatelů s odběrateli](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Další informace o tom, jak mohou dodavatelé používat spolupráci s dodavateli v procesech fakturace, uvádí téma [Pracovní prostor fakturace dodavatelské spolupráce](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Informace o zřizování nových uživatelů pro spolupráci s dodavateli uvádí téma [Správa uživatelů dodavatelské spolupráce](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Definování informací zobrazených dodavatelům při jejich reagování na nákupní objednávky
Když dodavatelé reagují na nákupní objednávky, které jim pošlete, zobrazí se dialogové okno, ve kterém musí potvrdit, zda objednávku přijmou, odmítnou nebo přijmou se změnami. Informace, které mají být zobrazeny v daném okamžiku dodavateli, můžou být specifické pro vaši firmu, takže můžete určit text, který se zobrazí ve všech třech potvrzovacích zprávách. Text například může informovat dodavatele o dalších krocích v procesu, nebo podmínkách a ujednáních.  

Chcete-li určit text, který se zobrazí v reakci na nákupní objednávky:

1.  Otevřete stránku **Informace pro dodavatele reagující na nákupní objednávky**.
2.  Vyberte jeden z typů odpovědí.
3.  Klikněte na možnost **Upravit.**
4.  Zadejte informace, které se mají dodavatelům zobrazit v poli **informační zpráva**.

Pokud je nutné přidat zprávy ve více jazycích, vytvořte samostatné zprávy s příslušnými jazykovými kódy. Dodavateli se zobrazí zpráva v jazyce, který používá.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Nastavení možností spolupráce pro konkrétního dodavatele
Obecné nastavení spolupráce dodavatele v Dynamics 365 for Operations konfiguruje správce. Například určují role zabezpečení, které jsou k dispozici pro všechny dodavatele, s nimiž spolupracujete. Existují také některá nastavení, která se můžou lišit pro každý účet dodavatele a měli byste je nastavit:

-   Povolte spolupráci s dodavatelem.
-   Rozhodněte, zda dodavatele může zobrazit informace o ceně.

### <a name="enable-vendor-collaboration"></a>Povolení spolupráce s dodavatelem.

Před vytvořením uživatelských účtů pro externí dodavatele nakonfigurujte účet dodavatele, aby mohli používat spolupráce dodavatele. Chcete-li to provést, nastavte pole **Aktivace spolupráce** na aktivní na kartě **Obecné** na stránce **Dodavatelé**. Existují dvě možnosti, které je možné vybrat:

-   **Aktivní (nákupní objednávky je automaticky potvrzena) **– nákupní objednávky se automaticky potvrzují poté, co je dodavatel přijme beze změn.
-   **Aktivní (nákupní objednávka není automaticky potvrzená) **-nákupní objednávky musí být ručně potvrzeny ve vaší organizaci poté, co je dodavatel přijal.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Rozhodnutí, zda dodavatele může zobrazit informace o ceně

Pokud chcete dodavateli sdělit informace o cenách, jako je jednotková cena, slevy a poplatky, přes rozhraní pro spolupráci, je nutné nastavit možnost **Ceny/částky nákupní objednávky** v účtu dodavatele na **Ano**. Tato možnost je k dispozici na kartě **Výchozí nastavení nákupní objednávky**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Práce s nákupními objednávkami při použití spolupráce dodavatele
### <a name="sending-a-po-to-the-vendor"></a>Odeslání nákupní objednávky dodavateli

Nákupní objednávky jsou připraveny v Dynamics 365 for Operations. V případě nákupní objednávky má stav **schváleno**, odeslat dodavateli pomocí ** odeslat potvrzení ** akce na **nákupní objednávky** stránky. Stav nákupní objednávky se změní na **V externí revizi**. Po odeslání nákupní objednávky ji může dodavatel zobrazit na stránce **Nákupní objednávky ke kontrole** rozhraní spolupráce dodavatele, kde ji může dodavatel přijmout, odmítnout nebo navrhnout její změny. Dodavatel může také přidat komentáře pro předávání informací, jako jsou například změny v nákupní objednávce. Pokud chcete tohoto dodavatele upozornit na novou nákupní objednávku, můžete také nákupní objednávky odeslat e-mailem pomocí systému správy tisku.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Potvrzení a přijetí nákupní objednávky dodavatelem

Když dodavatel potvrdí nákupní objednávku, může být nákupní objednávka automaticky potvrzena nebo může být nutné ji potvrdit ručně. To závisí na tom, zda ** aktivace dodavatele ** je nastaveno na **Active (nákupní objednávky je automaticky potvrzena)** pro dodavatele nebo na **Active (No není automaticky potvrzena)**.  

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
<td>Dodavatel <strong>přijme</strong> objednávku. Aplikace Dynamics 365 for Operations není nakonfigurována na automatické potvrzení nákupních objednávek, když je dodavatel přijme.</td>
<td>Stav objednávky bude aktualizován na hodnotu <strong>Potvrzeno</strong>. Pokud něco brání aktualizaci objednávky, odpověď dodavatele i tak bude zaznamenána jako <strong>Přijato</strong>, ale nákupní objednávka zůstane ve stavu <strong>Externí revize</strong>.</td>
</tr>
<tr class="odd">
<td>Dodavatel <strong>přijme</strong> objednávku. Aplikace Dynamics 365 for Operations je nakonfigurována na automatické potvrzení nákupních objednávek, když je dodavatel přijme.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Přijato</strong>, ale nákupní objednávka zůstane ve stavu <strong>Na externí kontrole</strong>.</td>
</tr>
<tr class="even">
<td>Dodavatel <strong>odmítne</strong> objednávku.</td>
<td>Odpověď dodavatele bude zaznamenána jako <strong>Zamítnuto</strong> a nákupní objednávka zůstane ve stavu <strong>Na externí kontrole</strong>. Odmítnutí je přijato společně s poznámkou pro dodavatele.</td>
</tr>
<tr class="odd">
<td>Dodavatel <strong>přijímá objednávky se změnami</strong>. Změny jsou navrženy na úrovni řádku. Je možné přijmout nebo odmítnout jednotlivé řádky. Další možné změny zahrnují:
<ul>
<li>Změna dat nebo množství.</li>
<li>Rozdělení řádků pro jiná data dodání nebo množství.</li>
<li>Nahrazení zboží.</li>
</ul>
Údaje o ceně a náklady nemůže změnit dodavatel. Návrhy na tyto změny mohou být provedeny pomocí poznámek.</td>
<td>Odpověď dodavatele je zaznamenána jako <strong>přijaty změny</strong>, <strong></strong>a zůstává stav PO <strong>externí revize</strong>.</td>
</tr>
</tbody>
</table>

Lze použít **nákupní objednávky****Příprava** pracovního prostoru sledování POs, které dodavatel reagoval na. Tento pracovní prostor obsahuje dva seznamy, které obsahují nákupní objednávky se stavem **externí revize**:

-   Na externí kontrole – vyžaduje akci.
-   Na externí kontrole čekající na odpověď dodavatele.

### <a name="changing-a-po"></a>Změna objednávky

Když je nutné změnit nákupní objednávku, na kterou dodavatel reagoval, můžete odeslat dodavateli prostřednictvím portálu novou verzi nákupní objednávky. Nová nákupní objednávka bude mít příponu, která značí, že se jedná o upravenou verzi nákupní objednávky té, která byla dříve předána. Stránka **Historie potvrzení nákupních objednávek dodavatele** slouží ke sledování historie každé objednávky. Dříve potvrzené verze nákupní objednávky zůstanou v seznamu potvrzených nákupních objednávek, dokud není potvrzena nová nákupní objednávka.

### <a name="cancelling-a-po"></a>Zrušení nákupní objednávky

Při zrušení objednávky je stav změněn na **Schváleno**. Je nutné odeslat nákupní objednávku zpět dodavateli prostřednictvím portálu pro dodavatele, aby dodavatel mohl dodavatel potvrdit nebo zamítnout zrušení. Po potvrzení zrušení se nákupní objednávka zobrazí v seznamu potvrzených nákupních objednávek jako **Zrušeno**.

### <a name="adding-attachments-to-a-po"></a>Přidání přílohy k nákupní objednávce

Můžete přidávat přílohy, například soubory obrázků a poznámky, do nákupní objednávky pomocí systému správy dokumentů. Přílohy přidané s omezením typu **Externí** dodavatel uvidí až poté, co mu pošlete nákupní objednávku.

## <a name="purchase-order-statuses-and-versions"></a>Stav a verze nákupní objednávky
Toto téma popisuje různé stavy, které může mít nákupní objednávka v době potvrzení a uvádí, v jakém bodě je nová verze nákupní objednávky dostupná dodavateli. Existují rozdíly v tomto, v závislosti na tom, zda použít Změna správy pro nákupní objednávky. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Verze a stavy, jestliže nepoužíváte správu změn

Následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Akce**                                                               | **Stav a verze**                                                                                                                                       |
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Dynamics 365 for Operations. | Stav je **Schváleno**.                                                                                                                                  |
| Nákupní objednávka je odeslána dodavateli.                                            | Verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.                                          |
| Dodavatel odešle odpověď **Přijata se změnami**.                  | Stav bude stále **Na externí kontrole**.                                                                                                                  |
| Provedete změny, které jsou požadovány dodavatelem.                  | Stav je změněn na **Schváleno**.                                                                                                                        |
| Odešlete novou verzi nákupní objednávky dodavateli.                        | Nová verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.                                      |
| Dodavatel přijme novou verzi nákupní objednávky.                            | Stav bude stále **Na externí revizi**, pokud není nakonfigurován účet dodavatele na nákupní objednávce na automatické nastavení stavu na **Potvrzeno** při přijetí. |

Dodavatelé nemusí nákupní objednávku potvrdit v rozhraní spolupráce pro dodavatele. Mohou také odeslat e-mailovou zprávu nebo sdělit jejich přijetí nákupní objednávky prostřednictvím jiných kanálů. Potvrďte objednávku ručně v aplikaci Dynamics 365 for Operations. V tomto případě se vám zobrazí upozornění, že objednávka má být potvrzena, přestože není reakce od dodavatele. Nákupní objednávka se poté zobrazí v historii potvrzení jako otevřená potvrzená objednávka, která nemá žádné odpovědi. Dále dodavatel již nemá možnost nákupní objednávku potvrdit nebo odmítnout.  

**Poznámka:** verze nákupní objednávky, která je dostupná pro jiné procesy v aplikaci Dynamics 365 for Operations, je vždy nejnovější verze, a to i v případě, že tato nebyla registrována v rozhraní pro spolupráci dodavatele.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Verze a stavy, jestliže používáte správu změn

Pokud povolíte správu změn pro nákupní objednávky, nákupní objednávky procházejí workflowem schválení, aby získaly stav **Schváleno**. Tento proces dodavateli není viditelný.  

Pokud je povolena Správa změn, následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít. Verze je registrována po schválení nákupní objednávky, nikoliv když je nákupní objednávka odeslána dodavateli nebo potvrzena.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Akce**                                                                                                    | **Stav a verze**                                                                                                                                                                                                                                                                                                                                                                      |
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Dynamics 365 for Operations.                                      | Stav majetku je **Koncept**.                                                                                                                                                                                                                                                                                                                                                                    |
| Nákupní objednávka je odeslána do schvalovacího procesu. (Toto je interní proces, kterého dodavatel není součástí). | Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávka není během procesu schvalování zamítnuta. Schválená nákupní objednávka je registrována jako verze.                                                                                                                                                                                                                     |
| Nákupní objednávka je odeslána dodavateli.                                                                                  | Verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.                                                                                                                                                                                                                                                                       |
| Provedete změny, které jsou požadovány dodavatelem.                                                       | Stav je opět změněn na **Koncept**.                                                                                                                                                                                                                                                                                                                                                    |
| Nákupní objednávka je opět odeslána do schvalovacího procesu.                                                            | Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávka není během procesu schvalování zamítnuta. Alternativně systém lze nakonfigurovat tak, aby změny konkrétního pole nevyžadovaly opětovné schválení. V tomto případě se stav nejprve změní na **Koncept**, a pak se automaticky aktualizuje na **Schváleno**. Schválená nákupní objednávka je registrována jako nová verze. |
| Odešlete novou verzi nákupní objednávky dodavateli.                                                             | Nová verze je registrována v rozhraní spolupráce dodavatele a stav se změní na **Na externí kontrole**.                                                                                                                                                                                                                                                                   |
| Dodavatel schválí novou verzi nákupní objednávky.                                                                | Stav se změní na **Potvrzeno** buď automaticky nebo když obdržíte odpověď od dodavatele a poté potvrdíte nákupní objednávku.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Sdílení informací o zásobách
Pokud používáte zásoby na skladě, dodavatelé mohou použít rozhraní spolupráce dodavatele k zobrazení informací na následujících stránkách:

-   **Nákupní objednávky spotřebovávající zásoby dodávek** – nákupní objednávky pro zásoby dodávek jsou generovány při změně vlastnictví zásob od dodavatele pro vaši společnost. Současně dojde k zaúčtování příjemky produktu. Tyto nákupní objednávky se zobrazí pouze na stránce **Nákupní objednávky spotřebovávající zásoby dodávek**. Nejsou zahrnuty na stránce **Všechny potvrzené nákupní objednávky** v modulu **Dodavatelská spolupráce**.
-   **Přijaté produkty ze zásob dodávky** - Tato stránka uvádí seznam všech transakcí, kde bylo vlastnictví produktů převedeno z dodavatele na vaši společnost. Tyto informace mohou dodavatelé použít k fakturaci zákazníkovi.
-   **Zásoby dodávky na skladě** - tato stránka zobrazuje zásoby dodávky na skladě vlastněné dodavatelem, které jsou k dispozici ve vašem skladu.





