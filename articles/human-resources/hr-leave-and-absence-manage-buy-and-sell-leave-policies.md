---
title: Správa zásad nákupu a prodeje pracovního volna
description: Zaměstnancům můžete povolit, aby kupovali a prodávali pracovní volno v Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429006"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Správa zásad nákupu a prodeje pracovního volna

[!include [banner](includes/preview-feature.md)]

Zaměstnancům můžete povolit koupi volna vytvořením zásad nákupu volna.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Povolit zaměstnancům, aby kupovali a prodávali pracovní volno

1. Na stránce **Parametry volna a nepřítomnosti** vyberte **Ano** pro **Umožněte zaměstnancům koupit pracovní volno**. 

## <a name="create-a-buy-leave-policy"></a>Vytvoření zásad nákupu volna

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**. 

2. Vyberte **Zásady nákupu a prodeje pracovního volna**.

3. Zvolte **Nové**.

4. Vložte **Název** a **Popis** pro zásady v **Zásady nákupu a prodeje pracovního volna**. 

5. Vyberte **Typ zásad**. 

   Dostupné typy zásad jsou **Množství** a **Hodiny za týden**. Vyberte **Množství** pro zadání **Pevné částky** pro maximální částky, které mohou zaměstnanci koupit a prodat. Pokud vyberete **Hodiny za týden**, k určení maximálního množství zásad použije pracovní doba definovaná v kalendáři přiřazené pracovní doby zaměstnance. 

6. Vyberte **počáteční datum** a **koncové datum** pro zásady. Žádosti o koupi nebo prodej vona budou k dispozici pouze v tomto časovém rámci. 

7. V **Zásadách nákupu** vyberte **Ekvivalent plného úvazku** (FTE) k rozdělení maximální částky na základě FTE definovaného na pozici zaměstnance. Pokud je typ zásad **Množství**, vložte **Maximální pevné množství**. 

8. Vyberte **Přidat**, chcete-li přidat typy pracovního volna pro zaměstnance, aby si mohli koupit volno. Do zásad můžete přidat více typů volna. 

9. Zadejte **Měsíce služby** pro typ volna, chcete-li povolit různé měsíce služby pro určení maximálního množství, které může zaměstnanec koupit. 

10. Zadejte **maximální množství** pro typ volna. 

11. Zadejte **Sazbu**, za kterou si zaměnstnanec koupí pracovní volno. 

12. Volitelně zadejte **Kód příjmů** pro použití při nákupu volna. 

13. Volitelně lze nastavit, zda použít FTE ke stanovení maximálního množství pro typ volna. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Přidejte do plánu volna a nepřítomnosti zásady nákupu a prodeje volna

1. Na stránce **Pracovní volno a nepřítomnost** vyberte plán volna a nepřítomnosti.

2. V **Pravidlech** vyberte **Zásady nákupu a prodeje pracovního volna**.

## <a name="see-also"></a>Viz také

[Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)</br>
[Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md)</br>
[Časově rozlišit plány pracovního volna a absence](hr-leave-and-absence-accrue.md)</br>
[Koupit a prodat pracovní volno](hr-employee-self-service-buy-sell-leave.md)

