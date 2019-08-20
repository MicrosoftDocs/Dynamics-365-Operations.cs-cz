---
title: Záruční listiny
description: Tento článek obsahuje informace o záručních listinách. V záruční listině banka souhlasí s platbou určité částky pro osobu, pokud jeden ze zákazníků banky neprovede požadovanou platbu nebo nesplní závazek vůči dané osobě.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e7ab2e66c378388d002d2f2090f89bf6c96dac2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842322"
---
# <a name="letters-of-guarantee"></a>Záruční listiny

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o záručních listinách. V záruční listině banka souhlasí s platbou určité částky pro osobu, pokud jeden ze zákazníků banky neprovede požadovanou platbu nebo nesplní závazek vůči dané osobě. 

Záruční listina je smlouva vydaná bankou (ručitelem), která zavazuje zaplatit peněžní částku určité osobě (příjemci), pokud klient banky (zmocnitel) nesplatí platbu nebo povinnost příjemci. Záruční listiny nejsou převoditelné. Vztahují se pouze na oprávněnou osobu, která je uvedena ve smlouvě. Zmocnitel může požadovat zvýšení nebo snížení hodnoty záruční listiny podléhající podmínkám smlouvy. 

Při likvidaci záruční listiny musí příjemci předložit původní záruční listinu a informovat banku o předchozí jistině před jejím datem konce platnosti. Banka pak vyplatí částku na účet příjemce podle podmínek v záruční listině. Banka rezervuje procento platby jako marži. Procento je dohodnuto a uvedeno v podmínkách smlouvy. 

Můžete vytvořit kód ke sledování účelu záruční listiny. Můžete také určit důvody, které lze přidružit k záruční listině při zrušení listiny. Kódy účelu a důvodu banky můžete zobrazit na stránkách **Kódy účelu platby** a **Banka – důvody**. 

Můžete použít stránku **Záruční listina** k dokončení těchto úloh:

-   Vytvoření správných položek hlavní knihy a eliminace ručního zadávání.
-   Zaznamenání všech peněžních a neměnových transakcí a sledování zůstatků záruční listiny.
-   Zaznamenání a sledování stavu a vypršení platnosti záruční listiny.
-   Generování sestavy se seznamem bank, které drží záruční listinu.

Následující tabulka popisuje akce, které lze provádět na záruční listině.

| Akce              | Účel                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| Odeslat do banky      | Odeslat bance žádost o vydání záruční listiny                                                                       |
| Přijmout z banky   | Jakmile banka odeslaný požadavek odsouhlasí, získat od banky záruční listinu.                            |
| Dát příjemci | Poté, co obdržíte od banky záruční listinu, poskytněte záruční listinu příjemci.              |
| Zvýšit hodnotu      | Pokud příjemce a zmocnitel souhlasí, zvyšte peněžní hodnotu.                                                  |
| Snížit hodnotu      | Pokud příjemce a zmocnitel souhlasí, snižte peněžní hodnotu.                                                  |
| Rozšířit              | Po poskytnutí záruční listiny příjemci rozšiřte dobu platnosti, pokud je to nutné. |
| Zrušit              | Smlouvu můžete ukončit, jakmile účel, pro který byla záruční listina vyžadována, pomine.                  |
| Likvidovat           | Jakmile příjemce předloží záruční listinu bance, vyplaťte záruční listinu.                      |


Další informace naleznete v následujících tématech:

[Transakce záruční listiny](tasks/letter-guarantee-transaction.md)

[Nastavení zařízení banky a zaúčtování profilů pro záruční listiny](tasks/set-up-bank-facilities-posting-profiles.md)


