---
title: Konfigurace parametrů pracovního volna a absence
description: Definujte parametry lidských zdrojů pro pracovní volno a absenci v Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197974"
---
# <a name="configure-leave-and-absence-parameters"></a>Konfigurace parametrů pracovního volna a absence

Před nastavením plánů pracovního volna a absencí v Dynamics 365 Human Resourcesje vhodné ověřit nastavení všech souvisejících parametrů lidských zdrojů, včetně následujících:

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

6. Na kartě **Pracovní volno a absence** ověřte nastavení FMLA a podle potřeby je změňte.

7. Zvolte **Uložit**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Zobrazen a zmena parametrů pracovního volna a absence

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Parametry pracovního volna a absence**.

3. Na kartě **Obecné** natavte následující parametry:
 
    - Nastavte **Jednotku pro pracovní vono a absenci** na hodiny nebo dny. Pokud se jedná o dny, můžete výběrem možnosti **Povolit definici poloviny dne** umožnit zaměstnancům výběr první nebo druhé poloviny dne ve svých žádostech o volno. 

    - Vyberte **Datum platnost měsíců služby**, pokud chcete nastavit, kdy se časové rozlišení uplatní pro plány volna za použití měsíců služby.

    - Vyberte **Výpočet zůstatku**, chcete-li zobrazit zůstatky k dnešnímu dni nebo k období časového rozlišení. Vyberete-li **Zůstatek k dnešnímu dni**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k dnešnímu dni. Pokud vyberete možnost **Zůstatek k období časového rozlišení**, zůstatek zobrazí součet všech časově rozlišených položek, úprav a požadavků k období časového rozlišení, které je definováno frekvencí plánu volna. 

## <a name="configure-calendar-parameters"></a>Konfigurace parametrů kalendáře

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Parametry pracovního volna a absence**.

3. Na kartě **Kalendář** podle potřeby ověřte nastavení kalendáře.

4. Zvolte **Uložit**.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
