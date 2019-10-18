---
title: Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy
description: V tomto tématu je popsán postup při dokončování hotových produktů ve výrobní zakázce do skladu, pokud registrační značka řídí dané skladové místo.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
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
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995135"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy 

Proces s názvem Hlášení jako dokončené dokončuje dokončené produkty ve výrobní zakázce do skladu. Je-li dokončený produkt povolen pro rozšířené skladové procesy, produkt je hlášen jako dokončený do skladového místa s názvem výrobního výstupu. Další informace o nastavení skladového výstupu naleznete v tématu [místo výstupu ve výrobě](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Chcete-li dokončit tento úkol, je nutné vybrat existující číslo registrační značky. Je-li výstupní místo výroby nastaveno tak, aby bylo sledováno podle registrační značky, musí být při vykazování produkčního výstupního místa jako dokončené zahrnuto číslo registrační značky. Pole **Registrační značka** je zobrazeno na výzvě **Průběh sestavy** na stránce **Zařízení karty úlohy**. Toto pole je viditelné ve výzvě **Průběh sestavy** při vykazování poslední operace výrobní zakázky. Toto pole se zobrazí pouze v případě, že je pro procesy správy skladu povolena položka pro výrobní zakázku. 
