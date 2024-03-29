---
title: Hledání za účelem navigace
description: Tento článek vysvětluje, jak používat funkci vyhledávání při přechodu na stránky.
author: jasongre
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.openlocfilehash: 4c362e4cd83f926e7e21d775abd24ae6ddfcbbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292330"
---
# <a name="navigation-search"></a>Hledání za účelem navigace

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Tento článek vysvětluje, jak používat funkci vyhledávání při přechodu na stránky.

Aplikace obsahuje několik oblastí a stránek na pomoc s prováděním různých úloh. Pokud potřebujete rychle najít stránky, které potřebujete k dokončení úkolů, použijte vyhledávací funkce navigace.

Chcete-li tuto funkci použít, kliknutím na ikonu **Hledat** zobrazíte pole **hledání**. Poté můžete zadat nejméně jedno slovo do pole. Systém vyhledá okamžitě příslušné stránky v aplikaci, které obsahují zadaná slova. Například můžete zadat jako vstup "fakturu dodavatele" a pak systém zobrazí výsledky odpovídající tomuto zadání.

> [!NOTE]
> Pole **hledání** usnadňuje hledání a přechod na stránky. Neslouží k hledání konkrétních dat nebo akcí.

![search-box.](media/navigation-search.png "Vyhledávací pole")

## <a name="quickly-navigate-to-a-particular-page"></a>Rychlý přechod na konkrétní stránku

Funkce hledání navigace slouží také jako skvělý způsob k rychlému přechodu na určitou stránku. Například pokud jste úředník pro závazky, který často používá stránku **Deník plateb**, můžete zadat "deník plateb" do pole **Vyhledávání**. Vzhledem k tomu, že vstup je přesná shoda nadpisu stránky, stránka je uvedena v horní části výsledků hledání a můžete na ni rychle přejít.

Seznam výsledků hledání obsahuje nadpis stránky a také cestu navigace. Zobrazuje umístění stránky v aplikaci. Rovněž pomáhá rozlišovat mezi dvěma nebo více podobnými stránkami ve výsledcích.

Při hledání stránky jsou zadané hodnoty porovnávány s nadpisem stránky a jeho cestou navigace. Pokud zadáte "pohledávky" do pole pro **vyhledávání**, budou výsledky pro stránky k dispozici v části Pohledávky - i v případě, i když nadpisy stránky nezahrnují slovo "pohledávky".

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Rychlý přechod na stránku na základě názvu technického formuláře

Funkce hledání navigace také zahrnuje velmi žádanou funkci pro pokročilé uživatele: schopnost rychle přejít na stránku na základě technického názvu formuláře. Mnoho uživatelů je tak obeznámeno se systémem, že znají přesné názvy formulářů, se kterými pracují. Pokud jste jedním z těchto uživatelů, můžete zadat **formulář:** a poté název formuláře, které hledáte. Zadáte-li například **formulář: vendinvoice**, výsledky hledání zobrazí všechny stránky, na kterých název formuláře začíná na **vendinvoice**.

## <a name="administration-and-security"></a>Správa a zabezpečení

Z pohledu správy a zabezpečení se funkce hledání navigace týká pouze následujících dvou typů výsledků:

- Stránky, které jsou povoleny v aktuální konfiguraci (pomocí konfiguračních klíčů).
- Stránky, ke kterým má uživatel přístup na základě role uživatele.

Seznam výsledků hledání je omezen na 10 položek. Pokud ve výsledcích nenaleznete, co jste hledali, doporučujeme upřesnit nebo aktualizovat zadání.

## <a name="development"></a>Vývoj

Z pohledu vývoje je funkce hledání navigace velmi jednoduchá, protože nevzniká téměř žádná prodleva mezi nasazením položek nabídky a možnosti jejich zobrazení ve výsledcích hledání. Dokud jsou položky nabídky propojeny z navigačního podokna nebo řídicího panelu, je možné je automaticky prohledávat.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
