---
title: Funkce elektronického výkaznictví ALLITEMS
description: Toto téma obsahuje obecné informace o použití funkce ALLITEMS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745386"
---
# <a name="allitems-er-function"></a><span data-ttu-id="12b42-103">Funkce elektronického výkaznictví ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="12b42-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12b42-104">Funkce `ALLITEMS` je spuštěna jako výběr v paměti a vrací novou sloučenou hodnotu typu *seznam záznamů* jako seznam záznamů, který představuje všechny položky odpovídající zadané cestě.</span><span class="sxs-lookup"><span data-stu-id="12b42-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12b42-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="12b42-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="12b42-106">Arguments</span></span>

<span data-ttu-id="12b42-107">`path`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="12b42-107">`path`: *Record list*</span></span>

<span data-ttu-id="12b42-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="12b42-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="12b42-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="12b42-109">Return values</span></span>

<span data-ttu-id="12b42-110">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="12b42-110">*Record list*</span></span>

<span data-ttu-id="12b42-111">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="12b42-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="12b42-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="12b42-112">Usage notes</span></span>

<span data-ttu-id="12b42-113">Cesta musí být definována jako platná cesta zdroje dat k prvku zdroje dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="12b42-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="12b42-114">Datové prvky, jako je řetězec a datum cesty, by měly zobrazit chybu v době návrhu v tvůrci výrazů elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="12b42-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="12b42-115">Nedoporučujeme používat tuto funkci pro transakční zdroje dat, které mohou obsahovat velký objem dat.</span><span class="sxs-lookup"><span data-stu-id="12b42-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="12b42-116">Místo toho zvažte použití funkce [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="12b42-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="12b42-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="12b42-117">Example 1</span></span>

<span data-ttu-id="12b42-118">Když zadáte `SPLIT("abcdef" , 2)` jako zdroj dat **DS**, výraz `COUNT( ALLITEMS (DS))` vrátí **"3"**.</span><span class="sxs-lookup"><span data-stu-id="12b42-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="12b42-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="12b42-119">Example 2</span></span>

<span data-ttu-id="12b42-120">Pokud zadáte **Vend** jako zdroj dat datového typu *seznam záznamů*, který odkazuje na tabulku aplikace VendTable, výraz `ALLITEMS (Vend.'<Relations'.ContactPerson)` vrátí sloučený seznam záznamů, který má strukturu tabulky **ContactPerson** a obsahuje všechny kontaktní osoby, ke kterým lze získat přístup pomocí relace **ContactPerson.ContactForParty == VendTable.Party**, a který je k dispozici všem dodavatelům (vendors) z odkazované tabulky dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="12b42-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12b42-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="12b42-121">Additional resources</span></span>

[<span data-ttu-id="12b42-122">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="12b42-122">List functions</span></span>](er-functions-category-list.md)
