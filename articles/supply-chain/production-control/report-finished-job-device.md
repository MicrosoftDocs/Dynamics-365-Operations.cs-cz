---
title: Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy
description: V tomto tématu je popsán postup při dokončování hotových produktů ve výrobní zakázce do skladu, pokud registrační značka řídí dané skladové místo.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092561"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy 

Proces s názvem Hlášení jako dokončené dokončuje dokončené produkty ve výrobní zakázce do skladu. Je-li dokončený produkt povolen pro rozšířené skladové procesy, produkt je hlášen jako dokončený do skladového místa s názvem výrobního výstupu. Další informace o nastavení skladového výstupu naleznete v tématu [místo výstupu ve výrobě](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Pokud je výstupní místo výroby řízeno registrační značkou, musí být při ohlášení dokončení k dispozici. Pole **Registrační značka** je zobrazeno na výzvě **Průběh sestavy** na stránce **Zařízení karty úlohy**. Toto pole je viditelné pouze na příznaku **Průběh sestavy**, pokud je pro procesy správy skladu povoleno vykazování na poslední operaci výrobní zakázky a zboží pro výrobní zakázku. 

Existují dvě možnosti poskytnutí licenčního štítku
- Uživatel vybere existující registrační značku v poli registrační značky.
- Registrační značka se automaticky generuje z číselné řady a převezme se v poli regitrační značka.

Možnost, aby byla značka licence automaticky generována, je konfigurována výběrem možnosti **Generovat registrační značku** na stránce **Konfigurovat kartu úlohy pro zařízení**.
