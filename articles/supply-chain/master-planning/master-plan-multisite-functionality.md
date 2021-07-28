---
title: Přehled hlavního plánování a funkce více pracovišť
description: Hlavní plánování bere v úvahu nastavení dimenzí zásob pracoviště a skladu.
author: roxanadiaconu
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2434"
- intro-internal
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65a1b7570466907e6b919f583db0bf553cbd542a
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335957"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Přehled hlavního plánování a funkce více pracovišť

[!include [banner](../includes/banner.md)]

Hlavní plánování bere v úvahu nastavení dimenzí zásob pracoviště a skladu. 

Dimenze pracoviště je povinná a dimenzi skladu lze nastavit jako povinnou.

Když je dimenze povinná, je nutné zadat její hodnotu ve všech skladových transakcích. Proto jsou při hlavním plánování známy pracoviště a sklad pro počáteční požadavek. Dimenze pracoviště je také konzistentní, aby se při rozpadu poptávky nižší úrovně nezměnila hodnota pracoviště.

Pokud není sklad nastavený jako povinný, je možné jej odvodit z počátečního požadavku. Plánovací modul musí na základě nastavení definovaných pro položku, jednotlivé sklady a podrobností řádku objednávky určit, který sklad se má použít.

Následující témata popisují, jak plánovací modul určuje používaný sklad při definici různých nastavení.

[Hlavní plánování pro disponibilitu pracoviště a skladu, sklad je povinný](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hlavní plánování pro disponibilitu pracoviště, povinný sklad](master-plan-site-coverage-warehouse-mandatory.md)

[Hlavní plánování pro disponibilitu pracoviště a skladu, sklad není povinný](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hlavní plánování pro disponibilitu pracoviště, sklad není povinný](master-plan-site-coverage-warehouse-not-mandatory.md)

[Určení verze kusovníku](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]