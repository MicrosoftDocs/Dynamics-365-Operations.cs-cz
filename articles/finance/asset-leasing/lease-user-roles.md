---
title: Přiřadit role uživatele leasingu
description: Tento článek popisuje role zabezpečení, které se používají pro leasing majetku. Vysvětluje také, jak těmto rolím přiřadit uživatele.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38c859d64742d582d0709506d83600ea26a21147
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878124"
---
# <a name="assign-lease-user-roles"></a>Přiřadit role uživatele leasingu

[!include [banner](../includes/banner.md)]

Tento článek popisuje role zabezpečení, které se používají pro leasing majetku. Vysvětluje také, jak těmto rolím přiřadit uživatele.

Při leasingu majetku rozlišují přístup tři uživatelské role. Jedna role je vhodná pro udržování leasingu, druhá je vhodná pro prohlížení leasingu a druhá je vhodná pro plnění povinností referenta leasingu. Každá role má specifická oprávnění pro všechny stránky leasingu a každá umožňuje uživatelům prohlížet, vytvářet, upravovat nebo mazat leasingy podle svých pracovních povinností.

| Role           | popis |
|----------------|-------------|
| Údržba leasingu | Uživatelé v této roli mohou přidávat, upravovat, mazat a zobrazovat leasingy. Tato role je určena pro každodenní uživatele, jejichž úkoly zahrnují vytváření a zveřejňování měsíčních záznamů deníku a přidávání nových leasingů. Tato role umožňuje přístup ke všem funkcím leasingu majetku. |
| Zobrazit leasing     | Uživatelé v této roli mohou prohlížet pouze záznamy leasingu, plány a spouštět sestavy. Nemohou vytvářet nové leasingy, upravovat stávající leasingy ani vytvářet záznamy deníku proti leasingům. Role je navržena pro uživatele, kteří musí pouze zobrazit leasingy, plány leasingu a transakce, které se proti těmto leasingům vyskytnou. |
| Referent leasingu    | Uživatelé v této roli mohou pouze vytvářet nové leasingy. Nemohou upravovat ani mazat existující leasingy, prohlížet plány leasingů ani zveřejňovat položky deníku leasingu. Tato role je určena pro uživatele, kteří pracují v kapacitě pro zadávání dat. |

Podle těchto pokynů můžete uživatelům přiřadit role, které se používají při leasingu majetku.

1. Přejděte na **Správa systému \> Zabezpečení \> Přiřadit uživatele k rolím**.
2. Vyberte role **Údržba leasingu**, **Referent leasingu** nebo **Zobrazit leasing** a poté vyberte **Ručně přiřadit / vyloučit uživatele**.
3. Vyberte uživatele, kterému chcete roli přiřadit, a poté vyberte **Přiřait k roli**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
