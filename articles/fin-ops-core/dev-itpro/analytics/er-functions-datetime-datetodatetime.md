---
title: Funkce el. výkaznictví DATETODATETIME
description: Toto téma obsahuje obecné informace o použití funkce DATETODATETIME elektronického výkaznictví.
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
ms.openlocfilehash: 961ccd18e70d4f9851027492366a7d9408a668c5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042405"
---
# <span data-ttu-id="d568c-103"><a name="DATETODATETIME">Funkce el. výkaznictví DATETODATETIME</a></span><span class="sxs-lookup"><span data-stu-id="d568c-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d568c-104">Funkce `DATETODATETIME` vrátí hodnotu typu *datum a čas*, která je převedena ze zadané hodnoty kalendářního data na hodnotu data a času ve koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="d568c-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="d568c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d568c-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="d568c-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="d568c-106">Arguments</span></span>

<span data-ttu-id="d568c-107">`date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="d568c-107">`date`: *Date*</span></span>

<span data-ttu-id="d568c-108">Hodnota data, která představuje datum pro převedení.</span><span class="sxs-lookup"><span data-stu-id="d568c-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="d568c-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="d568c-109">Return values</span></span>

<span data-ttu-id="d568c-110">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="d568c-110">*DateTime*</span></span>

<span data-ttu-id="d568c-111">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="d568c-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d568c-112">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="d568c-112">Example 1</span></span>

<span data-ttu-id="d568c-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` vrátí datum aktuální relace Microsoft Dynamics 365 Finance, 24. prosince 2015, **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="d568c-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="d568c-114">V tomto příkladu **CompInfo** představuje zdroj dat elektronického výkaznictví typu **Finance and Operations/Tabulka** a odkazuje na tabulku CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="d568c-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="d568c-115">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="d568c-115">Example 2</span></span>

<span data-ttu-id="d568c-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` vrátí hodnotu typu datum/čas **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="d568c-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d568c-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d568c-117">Additional resources</span></span>

[<span data-ttu-id="d568c-118">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="d568c-118">Date and time functions</span></span>](er-functions-category-datetime.md)
