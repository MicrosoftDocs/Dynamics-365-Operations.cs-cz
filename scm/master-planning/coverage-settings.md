---
title: "Nastavení pokrytí"
description: "Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>Nastavení pokrytí

[!include[banner](../includes/banner.md)]


Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku. 

Existuje několik způsobů, jak zadat nastavení disponibility:

-   Nastavte disponibilitu skupiny. Můžete vytvořit skupinu disponibility, která obsahuje nastavení pro všechny produkty spojené s touto skupinou disponibility. Klepněte na tlačítko **Master planning &gt;nastavení &gt;krytí &gt;skupiny disponibility** k vytvoření skupiny disponibility. Můžete propojit skupinu disponibility s produktem. Pokud je odkaz na konkrétní pracoviště, sklad nebo dimenze produktu, použijte pole **Skupina disponibility** na stránce **Disponibilita položky**. Pokud je propojení obecné, bez ohledu na dimenze produktu, použijte **Skupina disponibility** na pevné záložce **Plán** na stránce **Podrobnosti o produktu**. Pokud nespojíte skupinu disponibility s produktem, hlavní plánování bude ve výchozím nastavení používat **Obecná skupina disponibility**, která je určena na stránce **Parametry hlavního plánování**.

-   Nastavte disponibilitu produktu. Nastavení pokrytí lze vytvořit pro určitý produkt. Klepněte na tlačítko **řízení informací o produktech &gt;produkty &gt;uvolněných produktů**. Vyberte produkt, na **podokno akcí**, dále **plán** klepněte v **skupina disponibility**, klepněte na tlačítko **Disponibilita položky** otevřete **Disponibilita položky** stránky. Je-li produkt již spojen se skupinou disponibility, můžete nastavení skupiny disponibility přepsat v poli **Přepsat**. Nastavení disponibility na stránce** Disponibilita položky** má přednost před nastavením na stránce **Skupina disponibility**.

<!-- -->

-   Nastavení disponibility produktu pomocí průvodce. Průvodce vám pomůže nastavit parametry disponibility pro hlavní položku krok za krokem. Na stránce **Disponibilita položky** klepnutím na **Průvodce** otevřete **Průvodce disponibilitou položky**.

<!-- -->

-   Nastavení disponibility pro skupinu dimenzí. Klepněte na tlačítko **řízení informací o produktech &gt;běžné &gt;uvolněných produktů**. Na ** uvolnění produktu podrobnosti ** na stránce **Obecné** klepněte v **správy** seskupit, klikněte na **skupinu dimenze úložiště** odkaz. Na stránce **Skupina dimenze úložiště** vyberte pole **Plán disponibility podle dimenzí** a vytvořte tak nastavení disponibility pro dimenzi ve skupině dimenzí úložiště. Musí mít všechny dimenze produktu, jako je například konfigurace, barva, velikost, styl, **plán disponibility podle dimenzí** vybraného pole.



<a name="see-also"></a>Viz také
--------

[Master plans](master-plans.md)




