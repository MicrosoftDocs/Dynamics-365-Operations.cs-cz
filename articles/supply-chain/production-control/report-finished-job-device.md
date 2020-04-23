---
title: Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy
description: V tomto tématu je popsán postup při dokončování hotových produktů ve výrobní zakázce do skladu, pokud registrační značka řídí dané skladové místo.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211162"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="adc63-103">Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy</span><span class="sxs-lookup"><span data-stu-id="adc63-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="adc63-104">Proces s názvem Hlášení jako dokončené dokončuje dokončené produkty ve výrobní zakázce do skladu.</span><span class="sxs-lookup"><span data-stu-id="adc63-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="adc63-105">Je-li dokončený produkt povolen pro rozšířené skladové procesy, produkt je hlášen jako dokončený do skladového místa s názvem výrobního výstupu.</span><span class="sxs-lookup"><span data-stu-id="adc63-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="adc63-106">Další informace o nastavení skladového výstupu naleznete v tématu [místo výstupu ve výrobě](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="adc63-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="adc63-107">Pokud je výstupní místo výroby řízeno registrační značkou, musí být při ohlášení dokončení k dispozici.</span><span class="sxs-lookup"><span data-stu-id="adc63-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="adc63-108">Pole **Registrační značka** je zobrazeno na výzvě **Průběh sestavy** na stránce **Zařízení karty úlohy**.</span><span class="sxs-lookup"><span data-stu-id="adc63-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="adc63-109">Toto pole je viditelné pouze na příznaku **Průběh sestavy**, pokud je pro procesy správy skladu povoleno vykazování na poslední operaci výrobní zakázky a zboží pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="adc63-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="adc63-110">Existují dvě možnosti poskytnutí licenčního štítku</span><span class="sxs-lookup"><span data-stu-id="adc63-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="adc63-111">Uživatel vybere existující registrační značku v poli registrační značky.</span><span class="sxs-lookup"><span data-stu-id="adc63-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="adc63-112">Registrační značka se automaticky generuje z číselné řady a převezme se v poli regitrační značka.</span><span class="sxs-lookup"><span data-stu-id="adc63-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="adc63-113">Možnost, aby byla značka licence automaticky generována, je konfigurována výběrem možnosti **Generovat registrační značku** na stránce **Konfigurovat kartu úlohy pro zařízení**.</span><span class="sxs-lookup"><span data-stu-id="adc63-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
