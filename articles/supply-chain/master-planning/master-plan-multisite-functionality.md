---
title: Hlavní plánování a funkce více pracovišť
description: Hlavní plánování bere v úvahu nastavení dimenzí zásob pracoviště a skladu.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10981e0fe201566c83fd28c792000865bc533cd3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573084"
---
# <a name="master-planning-and-multisite-functionality"></a>Hlavní plánování a funkce více pracovišť

[!include [banner](../includes/banner.md)]

Hlavní plánování bere v úvahu nastavení dimenzí zásob pracoviště a skladu. 

Dimenze pracoviště je povinná a dimenzi skladu lze nastavit jako povinnou.

Když je dimenze povinná, je nutné zadat její hodnotu ve všech skladových transakcích. Proto jsou při hlavním plánování známy pracoviště a sklad pro počáteční požadavek. Dimenze pracoviště je také konzistentní, aby se při rozpadu poptávky nižší úrovně nezměnila hodnota pracoviště.

Pokud není sklad nastavený jako povinný, je možné jej odvodit z počátečního požadavku. Plánovací modul musí na základě nastavení definovaných pro položku, jednotlivé sklady a podrobností řádku objednávky určit, který sklad se má použít.

Následující témata popisují, jak plánovací modul určuje používaný sklad při definici různých nastavení.

[Hlavní plánování – disponibilita pracoviště a skladu, sklad povinný](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hlavní plánování – disponibilita pracoviště, sklad povinný](master-plan-site-coverage-warehouse-mandatory.md)

[Hlavní plánování – disponibilita pracoviště a skladu, sklad není povinný](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hlavní plánování – disponibilita pracoviště, sklad není povinný](master-plan-site-coverage-warehouse-not-mandatory.md)

[Hlavní plánování – jak se určuje verze kusovníku](master-plan-bom-version-determined.md)



