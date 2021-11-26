---
title: Správa zásad nákupu a prodeje pracovního volna
description: Zaměstnancům můžete povolit, aby kupovali a prodávali pracovní volno v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06682a81b09f90de0ef5eb1b656338e634f229db
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728874"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Správa zásad nákupu a prodeje pracovního volna

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Zaměstnancům můžete povolit koupi a prodej pracovního volna vytvořením zásad nákupu a prodeje pracovního volna. Tyto zásady můžete nakonfigurovat tak, aby používaly pracovní postup pro schvalování, nastavení maximálních částek a sazeb a nastavení sazeb pro nákup a prodej. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Povolit zaměstnancům, aby kupovali a prodávali pracovní volno

1. Na stránce **Parametry volna a absence** vyberte **Ano** pro **Umožnit zaměstnancům koupi pracovního volna** a **Umožnit zaměstnancům prodej pracovního volna**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Vytvoření zásady nákupu a prodeje pracovního volna

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**. 

2. Vyberte **Zásady nákupu a prodeje pracovního volna**.

3. Zvolte **Nové**.

4. Vložte **Název** a **Popis** pro zásady v **Zásady nákupu a prodeje pracovního volna**. 

5. Vyberte **Typ zásad**. 

   Dostupné typy zásad jsou **Množství** a **Hodiny za týden**. Vyberte **Množství** pro zadání **Pevné částky** pro maximální částky, které mohou zaměstnanci koupit a prodat. Pokud vyberete **Hodiny za týden**, k určení maximálního množství zásad použije pracovní doba definovaná v kalendáři přiřazené pracovní doby zaměstnance. 

6. Vyberte **počáteční datum** a **koncové datum** pro zásady. Žádosti o koupi nebo prodej vona budou k dispozici pouze v tomto časovém rámci. 

7. Vyberte **ID pracovního postupu** pro zásadu. Veškeré požadavky na nákup a prodej použijí tento pracovní postup ke kontrole a schválení. 

8. V **Zásadách nákupu** vyberte **Ekvivalent plného úvazku** (FTE) k rozdělení maximální částky na základě FTE definovaného na pozici zaměstnance. Pokud je typ zásad **Množství**, vložte **Maximální pevné množství**. 

9. Vyberte **Přidat**, chcete-li přidat typy pracovního volna pro zaměstnance, aby si mohli koupit volno. Do zásad můžete přidat více typů volna. 

10. Zadejte **Měsíce služby** pro typ volna, chcete-li povolit různé měsíce služby pro určení maximálního množství, které může zaměstnanec koupit. 

11. Zadejte **maximální množství** pro typ volna. 

12. Zadejte **Sazbu**, za kterou si zaměnstnanec koupí pracovní volno. 

13. Volitelně zadejte **Kód příjmů** pro použití při nákupu volna. 

14. Volitelně lze nastavit, zda použít FTE ke stanovení maximálního množství pro typ volna. 

15. Chcete-li vytvořit zásadu prodeje, postupujte podle kroků 8 až 14 pod částí **Zásada prodeje**. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Přidejte do plánu volna a nepřítomnosti zásady nákupu a prodeje volna

1. Na stránce **Pracovní volno a nepřítomnost** vyberte plán volna a nepřítomnosti.

2. V **Pravidlech** vyberte **Zásady nákupu a prodeje pracovního volna**.

## <a name="see-also"></a>Viz také

[Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)</br>
[Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md)</br>
[Časově rozlišit plány pracovního volna a absence](hr-leave-and-absence-accrue.md)</br>
[Koupit a prodat pracovní volno](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
