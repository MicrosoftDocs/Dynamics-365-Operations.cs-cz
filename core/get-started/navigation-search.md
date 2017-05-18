---
title: "Hledání za účelem navigace"
description: "V tomto tématu je vysvětleno, jak použít funkci vyhledávání k přechodu na stránky v aplikaci Microsoft Dynamics 365 for Operations."
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 650c8b60ba8204e8990cf607c1c9901b8f0bb762
ms.openlocfilehash: 9f2cbafa3e21006f458067baf99ea5abaef8bb86
ms.contentlocale: cs-cz
ms.lasthandoff: 04/28/2017


---

# <a name="navigation-search"></a>Hledání za účelem navigace

[!include[banner](../includes/banner.md)]


V tomto tématu je vysvětleno, jak použít funkci vyhledávání k přechodu na stránky v aplikaci Microsoft Dynamics 365 for Operations.

Microsoft Dynamics 365 for Operations poskytuje funkce pro celou řadu odvětví a vertikál. Aplikace obsahuje několik oblastí a stránek na pomoc s prováděním různých úloh. Pokud potřebujete rychle najít stránky, které potřebujete k dokončení úkolů, použijte vyhledávací funkce navigace. 

Chcete-li tuto funkci použít, kliknutím na ikonu **Hledat** zobrazíte pole **hledání**. Poté můžete zadat nejméně jedno slovo do pole. Systém vyhledá okamžitě příslušné stránky v aplikaci, které obsahují zadaná slova. Například můžete zadat jako vstup "fakturu dodavatele" a pak systém zobrazí výsledky odpovídající tomuto zadání. 

**Poznámka:** Pole **hledání** usnadňuje hledání a přechod na stránky. Neslouží k hledání konkrétních dat nebo akcí. 

[![Vyhledávací pole](media/navigation-search.png "Vyhledávací pole") 

## <a name="quickly-navigate-to-a-particular-page"></a>Rychlý přechod na konkrétní stránku
Funkce hledání navigace slouží také jako skvělý způsob k rychlému přechodu na určitou stránku. Například pokud jste úředník pro závazky, který často používá stránku **Deník plateb**, můžete zadat "deník plateb" do pole **Vyhledávání**. Vzhledem k tomu, že vstup je přesná shoda nadpisu stránky, stránka je uvedena v horní části výsledků hledání a můžete na ni rychle přejít. 

Seznam výsledků hledání obsahuje nadpis stránky a také cestu navigace. Zobrazuje umístění stránky v aplikaci. Rovněž pomáhá rozlišovat mezi dvěma nebo více podobnými stránkami ve výsledcích. 

Při hledání stránky jsou zadané hodnoty porovnávány s nadpisem stránky a jeho cestou navigace. Pokud zadáte "pohledávky" do pole **Hledání **, budou výsledky pro stránky k dispozici v části Pohledávky - i v případě, že nadpis stránka nezahrnuje slovo "pohledávky". 

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Rychlý přechod na stránku na základě názvu technického formuláře
Funkce hledání navigace také zahrnuje velmi žádanou funkci pro pokročilé uživatele: schopnost rychle přejít na stránku na základě technického názvu formuláře. Mnoho uživatelů je tak obeznámeno se systémem, že znají přesné názvy formulářů, se kterými pracují. Pokud jste jedním z těchto uživatelů, můžete zadat **formulář:** a poté název formuláře, které hledáte. Zadáte-li například **formulář: vendinvoice**, výsledky hledání zobrazí všechny stránky, na kterých název formuláře začíná na **vendinvoice**. 

## <a name="administration-and-security"></a>Správa a zabezpečení
Z pohledu správy a zabezpečení se funkce hledání navigace týká pouze následujících dvou typů výsledků:

-   Stránky, které jsou povoleny v aktuální konfiguraci (pomocí konfiguračních klíčů).
-   Stránky, ke kterým má uživatel přístup na základě role uživatele.

Seznam výsledků hledání je omezen na 10 položek. Pokud ve výsledcích nenaleznete, co jste hledali, doporučujeme upřesnit nebo aktualizovat zadání. 

## <a name="development"></a>Vývoj 
Z pohledu vývoje je funkce hledání navigace velmi jednoduchá, protože nevzniká téměř žádná prodleva mezi nasazením položek nabídky a možnosti jejich zobrazení ve výsledcích hledání. Dokud jsou položky nabídky propojeny z navigačního podokna nebo řídicího panelu, je možné je automaticky prohledávat. 

