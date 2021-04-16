---
title: Funkce el. výkaznictví JSONVALUE
description: Toto téma obsahuje obecné informace o použití funkce JSONVALUE elektronického výkaznictví.
author: NickSelin
ms.date: 12/11/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746356"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="ab35a-103">Funkce el. výkaznictví JSONVALUE</span><span class="sxs-lookup"><span data-stu-id="ab35a-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab35a-104">Funkce `JSONVALUE` analyzuje data ve formátu notace objektu JavaScript (JSON), který je dostupný v zadané cestě, a extrahuje skalární hodnotu se zadaným ID.</span><span class="sxs-lookup"><span data-stu-id="ab35a-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="ab35a-105">Poté vrátí extrahovanou skalární hodnotu jako *řetězcovou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ab35a-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab35a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab35a-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="ab35a-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="ab35a-107">Arguments</span></span>

<span data-ttu-id="ab35a-108">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="ab35a-108">`input`: *String*</span></span>

<span data-ttu-id="ab35a-109">Platná cesta ke zdroji dat typu *řetězec* obsahujícímu data JSON.</span><span class="sxs-lookup"><span data-stu-id="ab35a-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="ab35a-110">`path`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="ab35a-110">`path`: *String*</span></span>

<span data-ttu-id="ab35a-111">Identifikátor skalární hodnoty dat JSON.</span><span class="sxs-lookup"><span data-stu-id="ab35a-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="ab35a-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="ab35a-112">Return values</span></span>

<span data-ttu-id="ab35a-113">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="ab35a-113">*String*</span></span>

<span data-ttu-id="ab35a-114">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="ab35a-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ab35a-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="ab35a-115">Example</span></span>

<span data-ttu-id="ab35a-116">Zdroj dat **JsonField** obsahuje následující data ve formátu JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="ab35a-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="ab35a-117">V tomto případě výraz `JSONVALUE (JsonField, "BuildNumber")` vrátí následující hodnotu datového typu *řetězec*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="ab35a-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab35a-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ab35a-118">Additional resources</span></span>

[<span data-ttu-id="ab35a-119">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="ab35a-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]