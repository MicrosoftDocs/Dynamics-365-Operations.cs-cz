---
title: Nastavení frekvencí platby
description: Microsoft Dynamics 365 Human Resources používá frekvence plateb k výpočtu ročního platu zaměstnaneckých výhod, k určení částky prémie na výplatu zaměstnaneckých výhod, kterou zaměstnanec platí za každé výplatní období, a četnost plateb pro zprostředkovatele.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5d562b64a161891bf34b0dfa94fbf68325e21b5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417657"
---
# <a name="set-up-payment-frequencies"></a>Nastavení frekvencí platby

Microsoft Dynamics 365 Human Resources používá frekvence plateb k výpočtu ročního platu zaměstnaneckých výhod, k určení částky prémie na výplatu zaměstnaneckých výhod, kterou zaměstnanec platí za každé výplatní období, a četnost plateb pro zprostředkovatele.

Frekvence plateb zaměstnaneckých výhod používá převodní koeficienty pro převod období výplat zaměstnaneckých výhod mezi měsíční, čtrnáctidenní, dvoutýdenní, týdenní a denní frekvencí plateb. To umožňuje společnostem definovat vzájemnou závislost mezi jednotlivými frekvencemi plateb v rámci plánu zaměstnaneckých výhod.

Pole faktorů přepočtu identifikují faktor přepočtu z četnosti plateb do standardních platebních období a umožňují systému provádět výpočty mezi jednotlivými frekvencemi plateb. Částka faktoru přepočtu také určuje částku prémie na zaměstnanecké výhody, které má zaměstnanec zaplatit za každou frekvenci plateb.

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Frekvence plateb**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Frekvence plateb** | Jedinečný název frekvence plateb. |
   | **Popis** | Popis frekvence plateb. |
   | **Období** | Odpovídající období, které nejlépe odpovídá frekvenci plateb zaměstnaneckých výhod poskytovatelem a zaměstnancem. Seznam období se skládá ze standardních platebních období. |
   | **Počet platebních období** | Počet mzdových období, která představují, jak často jsou vypláceni poskytovatelé zaměstnaneckých výhod nebo zaměstnanci. Tato částka bude použita k výpočtu částky roční mzdy zaměstnance. |
   | **Roční koeficient převodu** | Roční koeficient převodu pro frekvenci plateb Roční koeficient převodu pro měsíční frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 1 rok) = 12 |
   | **Pololetní koeficient převodu** | Pololetní koeficient převodu pro frekvenci plateb Roční koeficient převodu pro pololetní frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 2krát ročně) = 6 |
   | **Čtvrtletní koeficient převodu** | Čtvrtletní koeficient převodu pro frekvenci plateb Čtvrtletní koeficient převodu pro pololetní frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 4 čtvrtletí) = 3 |
   | **Měsíční koeficient převodu** | Měsíční koeficient převodu pro frekvenci plateb Roční koeficient převodu pro měsíční frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 12 měsíců) = 1 |
   | **Čtrnáctidenní koeficient převodu** | Čtrnáctidenní koeficient převodu pro frekvenci plateb Roční koeficient převodu pro čtrnáctidenní frekvenci plateb je například následující: </br></br>(12 měsíčních plateb/24 (2x za měsíc)) = 0,5 | 
   | **Dvoutýdenní koeficient převodu** | Roční koeficient převodu pro frekvenci plateb Roční koeficient převodu pro měsíční frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 26 týdnů) = 0,461538 |
   | **Týdenní koeficient převodu** | Roční koeficient převodu pro frekvenci plateb Roční koeficient převodu pro měsíční frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 52 týdnů) = 0,230769 |
   | **Denní koeficient převodu** | Roční koeficient převodu pro frekvenci plateb Roční koeficient převodu pro měsíční frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 365 dní) = 0,032877 |
   | **Hodinový koeficient převodu** | Roční koeficient převodu pro frekvenci plateb Roční koeficient převodu pro měsíční frekvenci plateb je například následující: </br></br>(12 měsíčních plateb / 2080 hodin) = 0,005769

4. Zvolte **Uložit**. 
