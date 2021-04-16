---
title: Funkce el. výkaznictví ENUMERATE
description: Toto téma obsahuje obecné informace o použití funkce ENUMERATE elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746644"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="2d9e4-103">Funkce el. výkaznictví ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="2d9e4-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d9e4-104">Funkce `ENUMERATE` vrátí novou hodnotu typu *seznam záznamů*, která obsahuje výčtové záznamy zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="2d9e4-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d9e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d9e4-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="2d9e4-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="2d9e4-106">Arguments</span></span>

<span data-ttu-id="2d9e4-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="2d9e4-107">`list`: *Record list*</span></span>

<span data-ttu-id="2d9e4-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="2d9e4-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2d9e4-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2d9e4-109">Return values</span></span>

<span data-ttu-id="2d9e4-110">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="2d9e4-110">*Record list*</span></span>

<span data-ttu-id="2d9e4-111">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="2d9e4-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2d9e4-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="2d9e4-112">Usage notes</span></span>

<span data-ttu-id="2d9e4-113">Vrácený seznam výčtových záznamů dávek obsahuje následující dodatečné prvky:</span><span class="sxs-lookup"><span data-stu-id="2d9e4-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="2d9e4-114">Záznam polí (součást **Value**)</span><span class="sxs-lookup"><span data-stu-id="2d9e4-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="2d9e4-115">Aktuální index záznamů (součást **Number**)</span><span class="sxs-lookup"><span data-stu-id="2d9e4-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="2d9e4-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="2d9e4-116">Example</span></span>

<span data-ttu-id="2d9e4-117">Na následujícím obrázku je zdroj dat **Enumerated** vytvořen jako výčtový seznam záznamů dodavatelů ze zdroje dat **Vendors**, který odkazuje na tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="2d9e4-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="2d9e4-118">Následující ilustrace znázorňuje formát elektronického vykazování (ER).</span><span class="sxs-lookup"><span data-stu-id="2d9e4-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="2d9e4-119">V tomto formátu jsou vytvořeny vazby za účelem vygenerování výstupu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="2d9e4-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="2d9e4-120">Tento výstup představuje jednotlivé dodavatel jako výčtové uzly.</span><span class="sxs-lookup"><span data-stu-id="2d9e4-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="2d9e4-121">Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</span><span class="sxs-lookup"><span data-stu-id="2d9e4-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="2d9e4-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2d9e4-122">Additional resources</span></span>

[<span data-ttu-id="2d9e4-123">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="2d9e4-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]