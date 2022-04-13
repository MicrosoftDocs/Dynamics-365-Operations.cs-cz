---
title: Nastavení programů flexibilních kreditů
description: Programy pružného kreditu v aplikaci Microsoft Dynamics 365 Human Resources umožňují registrovat zaměstnance k zaměstnaneckým výhodám podle předem stanoveného počtu pružných kreditů.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1808d703983fd11e29f83c13f6181fb3068bc49
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533761"
---
# <a name="set-up-flex-credit-programs"></a>Nastavení programů flexibilních kreditů


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Programy pružného kreditu v aplikaci Microsoft Dynamics 365 Human Resources umožňují registrovat zaměstnance k zaměstnaneckým výhodám podle předem stanoveného počtu pružných kreditů. Zaměstnanci si mohou vybrat způsob přidělení pružných kreditů. Pokud má například zaměstnanec krytí v rámci plánu zdravotního pojištění partnera, může chtít použít kredity, které by se jinak používaly v oblasti zdravotního krytí k jiným dávkám. 

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **Programy pružných kreditů**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **ID kreditu zaměstnaneckých výhod** | Jedinečný identifikátor programu pro pružné kredity |
   | **Popis** | Popis programu pro pružné kredity. | 
   | **Od data** | Datum aktivace programu pružných kreditů. |
   | **Do data** | Koncové datum programu pružných kreditů. Můžete ponechat výchozí hodnotu (12/31/2154), která označuje, že pružný kredit nemá plánované vypršení platnosti. |
   | **Celková hodnota kreditu** | Počet kreditů, které bude každý zaměstnanec používat pro své zaměstnanecké výhody. |
   | **Pravidlo poměrného rozdělení** | Pravidlo, které se použije pro poměrné rozdělení pružných kreditů, když je zaměstnanec zařazen do středu pružného úvěrového období. </br></br><ul><li>**Žádné** – zaměstnanec neobdrží žádné pružné kredity, pokud nastoupí po začátku období programu pružných kreditů.</li><li>**Plný kredit** – zaměstnanec obdrží celou částku pružných kreditů bez ohledu na to, kdy byly přijaty.</li><li>**Poměrně rozložit** – zaměstnanec obdrží průběžnou částku pružných kreditů na základě počátečního data.</li></ul> |
   | **Vzorec poměrného rozdělení flexibilního kreditu** | Pravidlo, které se použije pro poměrné rozdělení pružných kreditů pro zaměstnance přijaté uprostřed období zaměstnaneckých výhod, když je zaměstnanec zařazen do středu pružného úvěrového období. Poměrné rozložení je založeno na počátečním datu zaměstnání. Toto pole se používá pouze tehdy, pokud vyberete **Poměrně rozložit** v poli **Pravidlo poměrného rozložení**. </br></br><ul><li>**Denně** – poměrně rozloží počet pružných kreditů, které zaměstnanec obdrží na úrovni dní. Celkový počet pružných kreditů je rozdělen podle počtu dní v daném období. Je-li například období zaměstnanecké výhody 400 dní, systém rozdělí celkový počet pružných kreditů na 400 za účelem výpočtu počtu pružných kreditů, které zaměstnanci obdrží za den.</li><li>**Aktuální měsíc** – vyjadřuje počet pružných kreditů, které zaměstnanec obdrží na úrovni měsíce zaokrouhlený na aktuální měsíc. Celkový počet pružných kreditů je rozdělen podle počtu měsíců v daném období. Je-li například období zaměstnanecké výhody 15 měsíců, systém rozdělí celkový počet pružných kreditů na 15 za účelem výpočtu počtu pružných kreditů, které zaměstnanci obdrží za měsíc.</li><li>**Následující měsíc** – vyjadřuje počet pružných kreditů, které zaměstnanec obdrží na úrovni měsíce zaokrouhlený na další měsíc. Celkový počet pružných kreditů je rozdělen podle počtu měsíců v daném období. Je-li například období zaměstnanecké výhody 15 měsíců, systém rozdělí celkový počet pružných kreditů na 15 za účelem výpočtu počtu pružných kreditů, které zaměstnanci obdrží za měsíc.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
