---
title: Funkce el. výkaznictví JSONVALUE
description: Toto téma obsahuje obecné informace o použití funkce JSONVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: d8209f8ce9d244ab7c82f897e4f59283e94e0522
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915664"
---
# <span data-ttu-id="f1de3-103"><a name="JSONVALUE">Funkce el. výkaznictví JSONVALUE</a></span><span class="sxs-lookup"><span data-stu-id="f1de3-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1de3-104">Funkce `JSONVALUE` analyzuje data ve formátu notace objektu JavaScript (JSON), který je dostupný v zadané cestě, a extrahuje skalární hodnotu se zadaným ID.</span><span class="sxs-lookup"><span data-stu-id="f1de3-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="f1de3-105">Poté vrátí extrahovanou skalární hodnotu jako *řetězcovou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f1de3-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1de3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1de3-106">Syntax</span></span>

```
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="f1de3-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="f1de3-107">Arguments</span></span>

<span data-ttu-id="f1de3-108">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="f1de3-108">`input`: *String*</span></span>

<span data-ttu-id="f1de3-109">Platná cesta ke zdroji dat typu *řetězec* obsahujícímu data JSON.</span><span class="sxs-lookup"><span data-stu-id="f1de3-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="f1de3-110">`path`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="f1de3-110">`path`: *String*</span></span>

<span data-ttu-id="f1de3-111">Identifikátor skalární hodnoty dat JSON.</span><span class="sxs-lookup"><span data-stu-id="f1de3-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1de3-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="f1de3-112">Return values</span></span>

<span data-ttu-id="f1de3-113">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f1de3-113">*String*</span></span>

<span data-ttu-id="f1de3-114">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="f1de3-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f1de3-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="f1de3-115">Example</span></span>

<span data-ttu-id="f1de3-116">Zdroj dat **JsonField** obsahuje následující data ve formátu JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="f1de3-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="f1de3-117">V tomto případě výraz `JSONVALUE (JsonField, "BuildNumber")` vrátí následující hodnotu datového typu *řetězec*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="f1de3-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1de3-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f1de3-118">Additional resources</span></span>

[<span data-ttu-id="f1de3-119">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="f1de3-119">Text functions</span></span>](er-functions-category-text.md)
