---
title: "Spolupráce s dodavateli pomocí portálu pro dodavatele"
description: "Toto téma vysvětluje, jak nákupčí mohou použít portál pro dodavatele pro spolupráci s externím dodavatelem během procesu potvrzení nákupní objednávky. Informace v tomto tématu platí pouze pro verze aplikace Dynamics AX z února a května 2016."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: f76e431320414b508728cbe9fe20456f107cbe40
ms.openlocfilehash: a8284e5a79e00def964b41f5c20bbb7377bf36be
ms.contentlocale: cs-cz
ms.lasthandoff: 06/09/2017

---

# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Spolupráce s dodavateli pomocí portálu pro dodavatele

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak nákupčí mohou použít portál pro dodavatele pro spolupráci s externím dodavatelem během procesu potvrzení nákupní objednávky. Informace v tomto tématu platí pouze pro verze aplikace Dynamics AX z února a května 2016.

Informace v tomto tématu platí pouze pro verze aplikace Dynamics AX z února a května 2016. Funkce portálu dodavatele byla v Dynamics 365 for Operations verze 1611 nahrazena rozšířenou funkcí spolupráce dodavatelů. Další informace o nové funkci spolupráce s dodavatelem naleznete v tématu [Používání spolupráce s dodavateli k práci s externími dodavateli](vendor-collaboration-work-external-vendors.md).  

Portál pro dodavatele je zaměřen na dodavatele, kteří nemají elektronické výměny dat (EDI) k dispozici v aplikaci Microsoft Dynamics AX pro výměnu informací o nákupních objednávkách. Portál umožňuje nákupčím odeslání nákupní objednávky dodavateli a obdržet odpovědi s potvrzením nebo odmítnutím přímo v Dynamics AX.  

Je možné nakonfigurovat proces tak, aby potvrzení od dodavatele automaticky potvrdilo objednávku. V tomto případě to znamená, že je v některých případech požadováno sledování, když je objednávka zamítnuta, nebo když je potvrzení dodavatele registrováno jako odpověď, ale stav nákupní objednávky nebyl z důvodu chyby v procesu potvrzení aktualizován na **Potvrzeno**.

## <a name="po-confirmation-and-rejection"></a>Potvrzení a odmítnutí nákupních objednávek
Nákupní objednávky jsou připraveny v aplikaci Dynamics AX. Pokud máte nákupní objednávky se stavem **Schváleno**, můžete je odeslat dodavateli vygenerováním požadavku na potvrzení. Pokud chcete tohoto dodavatele upozornit na novou nákupní objednávku, můžete také nákupní objednávky odeslat e-mailem pomocí systému správy tisku. Nákupní objednávka se zobrazí na portálu pro dodavatele s možností pro dodavatele ji potvrdit nebo zamítnout. Dodavatel může také přidat komentáře pro předávání informací, jako jsou například změny v nákupní objednávce.  

Na portálu pro dodavatele mohou dodavatelé zobrazit řádky objednávky. Tyto řádky obsahují informace, jako je například číslo externího produktu, dimenze, informace o cenách, množství, data dodání a dodací adresu. Dodavatel může generovat sestavy k zobrazení informací o nákupní objednávce a je také zobrazena celková cena. Náklady, které jsou relevantní pro dodavatele, se zobrazí, pokud dodavatel klepne na tlačítko **Náklady** v záhlaví nebo na řádcích. Dodavatelé mohou importovat informace o nákupní objednávce do vlastního systém pomocí funkce **Exportovat do aplikace Excel**.  

Následující tabulka zobrazuje typické výměny informací v závislosti na odpovědi dodavatele, když mu je odeslána objednávky k potvrzení.

| Typ odpovědi                                                                                                  | Výsledek                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dodavatel potvrdí objednávku. Systém je nakonfigurován na automatické potvrzení nákupních objednávek, když je dodavatel potvrdí.    | Stav objednávky bude aktualizován na hodnotu **Potvrzeno**. Pokud něco brání aktualizaci objednávky, odpověď dodavatele i tak bude zaznamenána jako **Potvrzeno**, ale nákupní objednávka zůstane ve stavu **Externí revize**.                                                                       |
| Dodavatel potvrdí objednávku. Systém není nakonfigurován na automatické potvrzení nákupních objednávek, když je dodavatel potvrdí. | Odpověď dodavatele bude zaznamenána jako **Potvrzeno**, ale nákupní objednávka zůstane ve stavu **Na externí kontrole**.                                                                                                                                                                                      |
| Dodavatel odmítne objednávku.                                                                                     | Odpověď dodavatele bude zaznamenána jako **Zamítnuto** a nákupní objednávka zůstane ve stavu **Na externí kontrole**. Odmítnutí je přijato společně s důvodem a návrhem změny, jako jsou například alternativní data. Nákupní objednávku aktualizujete a odešlete novou verzi pro potvrzení. |

## <a name="changes-to-a-po"></a>Změny v nákupní objednávce
Když je nutné změnit nákupní objednávku, která již byla potvrzena, můžete odeslat dodavateli prostřednictvím portálu pro dodavatele novou nákupní objednávku. Nová nákupní objednávka bude mít příponu, která značí, že se jedná o upravenou verzi nákupní objednávky té, která byla dříve předána. Portál pro dodavatele umožňuje dodavatelům sledování historie každé z objednávek. Dříve potvrzené verze nákupní objednávky zůstanou v seznamu potvrzených nákupních objednávek, dokud není potvrzena nová nákupní objednávka.  

Při zrušení objednávky je stav opět změněn na **Schváleno**. Je nutné odeslat nákupní objednávku zpět dodavateli prostřednictvím portálu pro dodavatele, aby dodavatel mohl dodavatel potvrdit nebo zamítnout zrušení. Po potvrzení zrušení se nákupní objednávka zobrazí v seznamu potvrzených nákupních objednávek jako **Zrušeno**.

## <a name="versions-status-transitions-and-change-management"></a>Verze, stavové převody a správa změn
Když je nákupní objednávka odeslána dodavateli, je registrována v systému jako konkrétní verze nákupní objednávky a stav se změní ze **Schváleno** na **Na externí kontrole**. Pokud objednávku změníte později, je vytvořena nová verze nákupní objednávky a stav přejde zpět na **Schváleno** (nebo se stav změní na **Koncept**, pokud je povolena správa změn).  

Následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít.

| Akce                                                   | Stav a verze                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Dynamics AX | Stav je **Schváleno**.                                                                           |
| Nákupní objednávka je odeslána do portálu pro dodavatele.                     | Verze je registrována na portálu pro dodavatele a stav se změní na **Na externí kontrole**.    |
| Provedete změny, které jsou požadovány dodavatelem.  | Stav je opět změněn na **Schváleno**.                                                            |
| Odešlete novou verzi nákupní objednávky na portál pro dodavatele. | Nová verze je registrována na portálu pro dodavatele a stav se změní na **Na externí kontrole**. |
| Dodavatel schválí novou verzi nákupní objednávky.           | Stav je změněn na **Potvrzeno**.                                                                |

Chcete-li zobrazit verze nákupní objednávky, které byly odeslány k dodavateli, a jejich odpovědi, klikněte z nákupní objednávky na možnost **Deníky** &gt; **Žádosti o potvrzení**.  

Objednávky, které byly odeslány dodavateli k odpovědi a nacházet ve stavu **Na externí kontrole** se buď objeví v seznamu **Nákupní objednávky odeslané na portál dodavatele, čekající na odpověď** nebo **Nákupní objednávky odeslané na portál dodavatele, odpověď vyžaduje akci**. Pokud změníte objednávku, která byla odeslána dodavateli, aby se stav změnil zpět na **Schváleno**, již se objednávka nezobrazuje v těchto seznamech. Pokud chcete zobrazit, zda došlo dříve ze strany dodavatele k odezvě na objednávku, klikněte na **Deníky** &gt; **Žádosti o potvrzení**.  

Dodavatelé nemusí nákupní objednávku potvrdit na portálu pro dodavatele. Mohou také odeslat e-mailovou zprávu nebo sdělit jejich přijetí nákupní objednávky prostřednictvím jiných kanálů. Potvrďte objednávku ručně v aplikaci Dynamics AX. V tomto případě se vám zobrazí upozornění, že objednávka má být potvrzena, přestože není reakce od dodavatele. Nákupní objednávka se poté zobrazí v historii potvrzení na portálu pro dodavatele jako otevřená potvrzená objednávka, která nemá žádné odpovědi. Dále dodavatel již nemá možnost nákupní objednávku potvrdit nebo odmítnout.  

**Poznámka:** verze nákupní objednávky, která je dostupná pro jiné procesy v aplikaci Dynamics AX, je vždy nejnovější verze, a to i v případě, že dosud daná verze nebyla registrována.

### <a name="change-management"></a>Správa změn

Pokud zapnete správu změn pro nákupní objednávky, nákupní objednávky prochází workflowem schválení, aby získala stav **Schváleno**. Tento proces dodavateli není viditelný.  

Pokud je správa změn povolena pro nákupní objednávku, verze je registrována po schválení nákupní objednávky, nikoliv když je nákupní objednávka odeslána dodavateli nebo potvrzena.  

Pokud je povolena Správa změn, následující tabulka zobrazuje příklad změn stavu a verze, kterou objednávka může projít.

| Akce                                                                                                        | Stav a verze                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Počáteční verze nákupní objednávky je vytvořena v aplikaci Dynamics AX                                                      | Stav majetku je **Koncept**.                                                                                                                                                                                                                                                                                                                                                                    |
| Nákupní objednávka je odeslána do schvalovacího procesu. (Toto je interní proces, kterého dodavatel není součástí). | Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávky není během procesu schvalování zamítnuta. Schválená nákupní objednávka je registrována jako verze.                                                                                                                                                                                                                     |
| Nákupní objednávka je odeslána do portálu pro dodavatele                                                                           | Verze je registrována na portálu pro dodavatele a stav se změní na **Na externí kontrole**.                                                                                                                                                                                                                                                                                        |
| Provedete změny, které jsou požadovány dodavatelem.                                                       | Stav je opět změněn na **Koncept**.                                                                                                                                                                                                                                                                                                                                                    |
| Nákupní objednávka je opět odeslána do schvalovacího procesu.                                                            | Stav je změněn z hodnoty **Koncept** na **Na kontrole** a na **Schválení**, pokud nákupní objednávky není během procesu schvalování zamítnuta. Alternativně systém lze nakonfigurovat tak, aby změny konkrétního pole nevyžadovaly opětovné schválení. V tomto případě se stav nejprve změní na **Koncept**, a pak se automaticky aktualizuje na **Schváleno**. Schválená nákupní objednávka je registrována jako nová verze. |
| Odešlete novou verzi nákupní objednávky na portál pro dodavatele.                                                      | Nová verze je registrována na portálu pro dodavatele a stav se změní na **Na externí kontrole**.                                                                                                                                                                                                                                                                                    |
| Dodavatel schválí novou verzi nákupní objednávky.                                                                | Stav se změní na **Potvrzeno** buď automaticky nebo když obdržíte odpověď od dodavatele a poté potvrdíte nákupní objednávku.                                                                                                                                                                                                                                                     |
<a name="see-also"></a>Viz také
--------

[Konfigurace zabezpečení pro uživatele portálu Spolupráce dodavatele](configure-security-vendor-portal-users.md)

[Pracovní prostor fakturace dodavatelské spolupráce](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace)




