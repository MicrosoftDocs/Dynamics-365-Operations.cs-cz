---
title: Seznam funkcí ER v kategorii kontejneru
description: Toto téma obsahuje informace o funkcích kontejneru, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561751"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="bd283-103">Seznam funkcí ER v kategorii kontejneru</span><span class="sxs-lookup"><span data-stu-id="bd283-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd283-104">[Kontejner elektronického výkaznictví (ER)](general-electronic-reporting.md) má [funkce](er-formula-language.md#functions), které lze použít k provádění operací zahrnujících zdroje dat datového typu *Kontejner*.</span><span class="sxs-lookup"><span data-stu-id="bd283-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="bd283-105">K těmto operacím dochází, když data zpracování představují kolekci binárních dat ve formátu binárního velkého objektu (BLOB).</span><span class="sxs-lookup"><span data-stu-id="bd283-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="bd283-106">Toto téma obsahuje souhrn těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="bd283-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="bd283-107">Seznam podporovaných funkcí</span><span class="sxs-lookup"><span data-stu-id="bd283-107">List of supported functions</span></span>

| <span data-ttu-id="bd283-108">Funkce</span><span class="sxs-lookup"><span data-stu-id="bd283-108">Function</span></span> | <span data-ttu-id="bd283-109">popis</span><span class="sxs-lookup"><span data-stu-id="bd283-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="bd283-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="bd283-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="bd283-111">Tato funkce vrací hodnotu *Kontejner*, která se skládá z binárního obsahu, který je dekódován ze zadaného řetězce ASCII, který představuje skupinu Base64 schémat kódování binárního textu.</span><span class="sxs-lookup"><span data-stu-id="bd283-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="bd283-112">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="bd283-112">Additional resources</span></span>

[<span data-ttu-id="bd283-113">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="bd283-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="bd283-114">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="bd283-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="bd283-115">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="bd283-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]