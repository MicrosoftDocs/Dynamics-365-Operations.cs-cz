---
title: Konfigurace parametrů pracovního volna a absence
description: Tento článek popisuje, jak definovat parametry lidských zdrojů pro dovolenou a nepřítomnost v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a39c74eef3865c03ccb9dd5aa2fece7f25e639a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891372"
---
# <a name="configure-leave-and-absence-parameters"></a>Konfigurace parametrů pracovního volna a absence

>[!Important]
>Funkce uvedené v tomto článku jsou aktuálně dostupné pro zákazníky používající samostatnou verzi aplikace Dynamics 365 Human Resources. Některé nebo všechny funkce budou dostupné jako součást budoucího vydání na infrastruktury Finance po vydání Finance 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Před nastavením plánů pracovního volna a absencí v Dynamics 365 Human Resources je vhodné ověřit nastavení všech souvisejících **Parametrů lidských zdrojů**, včetně následujících:

- Číselná řada pro požadavky na pracovní volno
- Nastavení zákona Opuštění z rodinných a lékařských důvodu (FMLA)
- Nastavení samoobslužných služeb pro zaměstnance pro požadavky na pracovní volno a absenci
- Parametry pracovního volna a absence

## <a name="view-and-change-human-resources-parameters"></a>Zobrazení a změna parametrů lidských zdrojů

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **parametry lidských zdrojů**.

3. Na kartě **číselné řady** ověřte **kód číselné řady** pro **ID žádosti o pracovní volno** a podle potřeby jej změňte. Toto nastavení určuje pořadí používané pro automatické přiřazování ID k žádostem o pracovní volno.

4. Na kartě **FMLA** ověřte nastavení FMLA a podle potřeby je změňte.

5. Na kartě **Samoobsluha zaměstnance** určete, zda manažeři mohou zadat žádosti o pracovní volno a absenci jménem svých zaměstnanců.

7. Zvolte **Uložit**.

>[!IMPORTANT]
>Zobrazení pracovního volna a absencí napříč společnostmi je aktuálně ve verzi Preview. Tuto funkci budete muset povolit v prostředí **Sandbox**, aby se vám zobrazila možnost pracovního volna a absencí. Další informace o povolení funkcí verze Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Zobrazení a změna sdílených parametrů Human Resources

1. Na stránce **Správa zaměstnanců** vyberte kartu **Odkazy**.

2. V části **Nastavení** vyberte **Sdílené parametry Human Resources**.

3. Na kartě **Rozšířený přístup** vyberte **Ano** pro **Povolit zobrazení pracovního volna mezi společnostmi**, abyste umožnili prohlížet pracovní volno napříč společností.

4. Zvolte **Uložit**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Zobrazen a zmena parametrů pracovního volna a absence

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Parametry pracovního volna a absence**.

3. Na kartě **Obecné** natavte následující parametry:
 
    - Nastavte **Jednotku pro pracovní vono a absenci** na hodiny nebo dny. Pokud se jedná o dny, můžete výběrem možnosti **Povolit definici poloviny dne** umožnit zaměstnancům výběr první nebo druhé poloviny dne ve svých žádostech o volno. 

    - Vyberte **Datum platnost měsíců služby**, pokud chcete nastavit, kdy se časové rozlišení uplatní pro plány volna za použití měsíců služby.

    - Vyberte **Výpočet zůstatku**, chcete-li zobrazit zůstatky k dnešnímu dni nebo k období časového rozlišení. Vyberete-li **Zůstatek k dnešnímu dni**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k dnešnímu dni. Pokud vyberete možnost **Zůstatek k období časového rozlišení**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k období časového rozlišení, které je definováno frekvencí plánu volna. 

    - Nastavte **Čas zahájení** dávkové úlohy **Vypršení platnosti převodu do dalšího období**.  
    
    - Vyberte **Ano** pro **Umožnit zaměstnancům koupi pracovního volna** a **Umožnit zaměstnancům prodej pracovního volna**. Pokud vyberete **Ano** pro tyto možnosti, můžete vytvořit zásady koupi a prodeje pracovního volna a umožnit zaměstnancům odesílat žádosti o koupi a prodej pracovního volna.

## <a name="configure-calendar-parameters"></a>Konfigurace parametrů kalendáře

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Parametry pracovního volna a absence**.

3. Na kartě **Kalendář** podle potřeby ověřte nastavení kalendáře.

4. Zvolte **Uložit**.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
