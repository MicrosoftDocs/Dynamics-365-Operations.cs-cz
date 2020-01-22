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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915986"
---
# <span data-ttu-id="7f668-103"><a name="GETCURRENTCOMPANY">Funkce el. výkaznictví GETCURRENTCOMPANY</a></span><span class="sxs-lookup"><span data-stu-id="7f668-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f668-104">Funkce `GETCURRENTCOMPANY` vrátí hodnotu typu *řetězec*, která představuje kód právnické osoby (společnosti), ke které je uživatel momentálně přihlášen.</span><span class="sxs-lookup"><span data-stu-id="7f668-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f668-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f668-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="7f668-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="7f668-106">Return values</span></span>

<span data-ttu-id="7f668-107">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="7f668-107">*String*</span></span>

<span data-ttu-id="7f668-108">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="7f668-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7f668-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="7f668-109">Example</span></span>

<span data-ttu-id="7f668-110">`GETCURRENTCOMPANY ()` vrátí hodnotu **USMF** u uživatele přihlášeného ke společnosti **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="7f668-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f668-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7f668-111">Additional resources</span></span>

[<span data-ttu-id="7f668-112">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="7f668-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
