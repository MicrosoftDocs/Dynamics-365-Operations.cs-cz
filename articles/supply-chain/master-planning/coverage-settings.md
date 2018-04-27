---
title: "Nastavení pokrytí"
description: "Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a>Nastavení pokrytí

[!INCLUDE [banner](../includes/banner.md)]

Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku. 

Existuje několik způsobů, jak zadat nastavení disponibility:

-   Nastavte disponibilitu skupiny. Můžete vytvořit skupinu disponibility, která obsahuje nastavení pro všechny produkty spojené s touto skupinou disponibility. Klikněte na tlačítko **Hlavní plánování &gt; Nastavení &gt; Disponibilita &gt; Skupiny disponibility** a vytvořte tak skupinu disponibility. Můžete propojit skupinu disponibility s produktem. Pokud je odkaz na konkrétní pracoviště, sklad nebo dimenze produktu, použijte pole **Skupina disponibility** na stránce **Disponibilita položky**. Pokud je propojení obecné, bez ohledu na dimenze produktu, použijte **Skupina disponibility** na pevné záložce **Plán** na stránce **Podrobnosti o produktu**. Pokud nespojíte skupinu disponibility s produktem, hlavní plánování bude ve výchozím nastavení používat **Obecná skupina disponibility**, která je určena na stránce **Parametry hlavního plánování**.

-   Nastavte disponibilitu produktu. Nastavení pokrytí lze vytvořit pro určitý produkt. Klikněte na možnosti **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**. Vyberte produkt v **podokně akcí** na kartě **Plán** a ve **skupině disponibility**otevřete kliknutím na tlačítko **Disponibilita položky** stránku **Disponibilita položky**. Je-li produkt již spojen se skupinou disponibility, můžete nastavení skupiny disponibility přepsat v poli **Přepsat**. Nastavení disponibility na stránce**Disponibilita položky** má přednost před nastavením na stránce **Skupina disponibility**.

<!-- -->

-   Nastavení disponibility produktu pomocí průvodce. Průvodce vám pomůže nastavit parametry disponibility pro hlavní položku krok za krokem. Na stránce **Disponibilita položky** klepnutím na **Průvodce** otevřete **Průvodce disponibilitou položky**.

<!-- -->

- Nastavení disponibility pro skupinu dimenzí. Klikněte na <strong>Řízení informací o produktech &gt; Společné &gt; Uvolněné produkty</strong>. Na stránce <strong>Podrobnosti o uvolněném produktu** na kartě **Hlavní</strong> ve skupině <strong>Správa</strong> klepněte na odkaz <strong>Skupina dimenze úložiště</strong>. Na stránce <strong>Skupina dimenze úložiště</strong> vyberte pole <strong>Plán disponibility podle dimenzí</strong> a vytvořte tak nastavení disponibility pro dimenzi ve skupině dimenzí úložiště. Všechny dimenze produktu, například jako konfigurace, barva, velikost nebo styl, musí mít vybráno pole <strong>Plán disponibility podle dimenzí</strong>.



<a name="see-also"></a>Viz také
--------

[Hlavní plány](master-plans.md)




