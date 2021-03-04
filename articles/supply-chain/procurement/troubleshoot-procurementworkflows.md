---
title: Řešení problémů s pracovními postupy zásobování a zdrojů
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s pracovními postupy zásobování a zdrojů.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424239"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Řešení problémů s pracovními postupy zásobování a zdrojů

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s pracovními postupy zásobování a zdrojů.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Chyba při opětovném odeslání nákupní objednávky do pracovního postupu po změně: „Změny nákupní objednávky X jsou povoleny pouze ve stavu konceptu, když je aktivována správa změn“

K tomuto problému dochází, pouze pokud byla nákupní objednávka ve stavu *Potvrzeno* před požadováním změn. Pokud požadujete změny, když je objednávka ve stavu *Schváleno*, lze pracovní postup úspěšně zpracovat.

### <a name="error-description"></a>Popis chyby

Při opakovaném odeslání nákupní objednávky po změně dojde v pracovním postupu k následující chybě:

> Zastaveno (chyba): Výjimka X++: Změny nákupní objednávky PO0000569 jsou povoleny pouze ve stavu Koncept, když je aktivována správa změn na<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Řešení problému

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problém bude vyřešen prostřednictvím [tohoto článku znalostní báze Microsoft](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno.

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Pokud je zbytek dodávky zrušen u nákupní objednávky, kde je zapnuta správa změn, přejde nákupní objednávka do stavu Potvrzeno.

### <a name="issue-description"></a>Popis problému

Pokud je u nákupní objednávky, která podléhá správě změn, jedinou požadovanou změnou zrušení zbytku dodávky na jednom nebo více řádcích, přejde nákupní objednávka přímo do stavu *Potvrzeno*, když je schválena, a nebude vytvořen žádný deník.

### <a name="issue-resolution"></a>Řešení problému

Zrušení zbytku dodávky nemá vliv na obsah deníku potvrzení. Tato funkce by měla být použita, když byl řádek částečně přijat, a zbývající kvalita by měla být zrušena v kroku procesu po potvrzení nákupní objednávky u dodavatele.

Pokud by se to mělo projevit v potvrzení nákupní objednávky, mělo by být množství upraveno na řádku nákupní objednávky tak, aby bylo vyžadováno potvrzení. Popřípadě pokud na řádku nic nebylo přijato, lze množství odebrat. V takovém případě bude vyžadováno opětovné potvrzení.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Zrušené nákupní objednávky se zobrazí v seznamu konceptů v pracovním prostoru Příprava nákupní objednávky.

### <a name="issue-description"></a>Popis problému

Po zrušení nákupních objednávek, které byly ve stavu *Potvrzeno* se zrušené nákupní objednávky stále zobrazují v seznamu konceptů nákupních objednávek v pracovním prostoru **Příprava nákupní objednávky**.

### <a name="issue-resolution"></a>Řešení problému

K tomuto problému dochází pouze u nákupních objednávek, které podléhají správě změn. Dochází k tomu, protože zrušení je považováno za změnu, kterou je nutné schválit. Schválení může být provedeno automaticky systémem. Proto je procesem odeslání zrušené nákupní objednávky do pracovního postupu schválení, aby mohla přejít do stavu *Schváleno*. V tomto okamžiku se nákupní objednávka již nebude zobrazovat v seznamu konceptů nákupních objednávek v pracovním prostoru **Příprava nákupní objednávky**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]