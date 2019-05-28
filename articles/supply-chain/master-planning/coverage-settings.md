---
title: Nastavení distponibility
description: Toto téma poskytuje informace o nastavení disponibility, které hlavní plánování používá k výpočtu požadavků na položky.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538887"
---
# <a name="coverage-settings"></a>Nastavení distponibility

[!include [banner](../includes/banner.md)]

Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku.

Existuje několik způsobů, jak zadat nastavení disponibility:

- Nastavte disponibilitu skupiny.

    Můžete vytvořit skupinu disponibility, která obsahuje nastavení pro všechny produkty spojené s touto skupinou disponibility. Přejděte na **Hlavní plánování &gt; Nastavení &gt; Disponibilita &gt; Skupiny disponibility** a vytvořte tak skupinu disponibility. Můžete propojit skupinu disponibility s produktem. Pokud je odkaz na konkrétní pracoviště, sklad nebo dimenze produktu, použijte pole **Skupina disponibility** na stránce **Disponibilita položky**. Pokud je propojení obecné, bez ohledu na dimenze produktu, použijte pole **Skupina disponibility** na pevné záložce **Plán** stránky **Podrobnosti o produktu**. Pokud ve výchozím nastavení nespojíte skupinu disponibility s produktem, hlavní plánování bude používat obecnou skupinu disponibility, která je určena na stránce **Parametry hlavního plánování**.

- Nastavte disponibilitu produktu.

    Nastavení pokrytí lze vytvořit pro určitý produkt. Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**. Vyberte produkt a pak v podokně akcí na kartě **Plán** ve **skupině disponibility** zvolte **Disponibilita položky** pro otevření stránky **Disponibilita položky**. Je-li produkt již spojen se skupinou disponibility, můžete nastavení skupiny disponibility přepsat v poli **Přepsat**. Nastavení disponibility na stránce**Disponibilita položky** má přednost před nastavením na stránce **Skupina disponibility**.

- Nastavení disponibility produktu pomocí průvodce.

    Průvodce vás provede jednotlivými kroky procesu nastavení parametrů disponibility primární položky. Na stránce **Disponibilita položky** v podokně akcí zvolte **Průvodce** a otevřete **Průvodce disponibilitou položky**.

- Nastavení disponibility pro skupinu dimenzí.

    Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**. Na stránce **Podrobnosti o uvolněném produktu** na záložce s náhledem **Obecné** v části **Správa** zvolte odkaz v poli **Skupina dimenze úložiště**. Na stránce **Skupiny dimenze úložiště** vyberte zaškrtávací pole **Plán disponibility podle dimenzí** a vytvořte tak nastavení disponibility pro dimenzi ve skupině dimenzí úložiště. Pole **Plán disponibility podle dimenzí** musí mít vybráno pro všechny dimenze produktu, jako je například konfigurace, barva, velikost nebo styl.

## <a name="additional-resources"></a>Další zdroje

[Hlavní plány](master-plans.md)
