---
title: Funkce elektronického výkaznictví ALLITEMSQUERY
description: Toto téma obsahuje obecné informace o použití funkce ALLITEMSQUERY elektronického výkaznictví.
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746692"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="12528-103">Funkce elektronického výkaznictví ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="12528-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12528-104">Funkce `ALLITEMSQUERY` je spuštěna jako připojený dotaz SQL.</span><span class="sxs-lookup"><span data-stu-id="12528-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="12528-105">Vrátí novou sloučenou hodnotu typu *seznam záznamů*, která se skládá ze seznamu záznamů představujících všechny položky, které odpovídají zadané cestě.</span><span class="sxs-lookup"><span data-stu-id="12528-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="12528-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12528-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="12528-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="12528-107">Arguments</span></span>

<span data-ttu-id="12528-108">`path`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="12528-108">`path`: *Record list*</span></span>

<span data-ttu-id="12528-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="12528-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="12528-110">Musí obsahovat alespoň jednu relaci.</span><span class="sxs-lookup"><span data-stu-id="12528-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="12528-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="12528-111">Return values</span></span>

<span data-ttu-id="12528-112">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="12528-112">*Record list*</span></span>

<span data-ttu-id="12528-113">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="12528-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="12528-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="12528-114">Usage notes</span></span>

<span data-ttu-id="12528-115">Zadaná cesta musí být definována jako platná cesta zdroje dat k prvku zdroje dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="12528-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="12528-116">Musí také obsahovat alespoň jednu relaci.</span><span class="sxs-lookup"><span data-stu-id="12528-116">It must also contain at least one relation.</span></span> <span data-ttu-id="12528-117">Datové prvky, jako je *řetězec* a *datum* cesty, by měly zobrazit chybu v době návrhu v tvůrci výrazů elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="12528-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="12528-118">Pokud je tato funkce použita pro zdroje dat typu *seznam záznamů*, které odkazují na objekt aplikace, který lze přímo volat pomocí jazyka SQL (například tabulka, entita nebo dotaz), je spuštěna jako připojený dotaz SQL.</span><span class="sxs-lookup"><span data-stu-id="12528-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="12528-119">V opačném případě běží v paměti jako funkce [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="12528-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="12528-120">Příklad</span><span class="sxs-lookup"><span data-stu-id="12528-120">Example</span></span>

<span data-ttu-id="12528-121">Definujte v mapování modelu následující zdroje dat:</span><span class="sxs-lookup"><span data-stu-id="12528-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="12528-122">Zdroj dat **CustInv** typu *záznamy tabulky*, který odkazuje na tabulku CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="12528-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="12528-123">Zdroj dat **FilteredInv** typu *vypočítané pole*, který obsahuje výraz `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="12528-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="12528-124">Zdroj dat **JourLines** typu *vypočítané pole*, který obsahuje výraz `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="12528-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="12528-125">Při spuštění mapování modelu k volání zdroje dat **JourLines** se spustí příkaz SQL:</span><span class="sxs-lookup"><span data-stu-id="12528-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="12528-126">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="12528-126">Additional resources</span></span>

[<span data-ttu-id="12528-127">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="12528-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]