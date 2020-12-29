---
title: Funkce el. výkaznictví GETCURRENTCOMPANY
description: Toto téma obsahuje obecné informace o použití funkce GETCURRENTCOMPANY elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e14c6a8aaff0a32a115117938d0e853bb34bb14
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684852"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="62099-103">Funkce el. výkaznictví GETCURRENTCOMPANY</span><span class="sxs-lookup"><span data-stu-id="62099-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62099-104">Funkce `GETCURRENTCOMPANY` vrátí hodnotu typu *řetězec*, která představuje kód právnické osoby (společnosti), ke které je uživatel momentálně přihlášen.</span><span class="sxs-lookup"><span data-stu-id="62099-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="62099-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62099-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="62099-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="62099-106">Return values</span></span>

<span data-ttu-id="62099-107">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="62099-107">*String*</span></span>

<span data-ttu-id="62099-108">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="62099-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="62099-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="62099-109">Example</span></span>

<span data-ttu-id="62099-110">`GETCURRENTCOMPANY ()` vrátí hodnotu **USMF** u uživatele přihlášeného ke společnosti **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="62099-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62099-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="62099-111">Additional resources</span></span>

[<span data-ttu-id="62099-112">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="62099-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
