---
title: Hmotnost musí být kladná
description: Hmotnost musí být kladná
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924296"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="01e6b-103">Hmotnost musí být kladná</span><span class="sxs-lookup"><span data-stu-id="01e6b-103">Weight must be positive</span></span>

<span data-ttu-id="01e6b-104">Kód chyby: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="01e6b-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="01e6b-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="01e6b-105">Symptoms</span></span>

<span data-ttu-id="01e6b-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="01e6b-106">The system shows the following error message:</span></span>

> <span data-ttu-id="01e6b-107">Hmotnost musí být kladná.</span><span class="sxs-lookup"><span data-stu-id="01e6b-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="01e6b-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="01e6b-108">Cause</span></span>

<span data-ttu-id="01e6b-109">Pole **Hrubá hmotnost** je nastaveno na hodnotu *0* (nula) nebo na zápornou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01e6b-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="01e6b-110">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="01e6b-110">Resolution</span></span>

<span data-ttu-id="01e6b-111">Chcete-li zadat hmotnost, proveďte jeden z následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="01e6b-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="01e6b-112">V poli **Hrubá hmotnost** nastavte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01e6b-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="01e6b-113">Poté vyberte jednotku z rozevíracího seznamu.</span><span class="sxs-lookup"><span data-stu-id="01e6b-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="01e6b-114">Výběrem možnosti **Získat systémovou hmotnost** vypočítejte hodnotu **Hrubá hmotnost**.</span><span class="sxs-lookup"><span data-stu-id="01e6b-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
