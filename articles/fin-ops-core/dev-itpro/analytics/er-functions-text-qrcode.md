---
title: Funkce elektronického výkaznictví QRCODE
description: Toto téma obsahuje obecné informace o použití funkce QRCODE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 8a52dbce29140591baf4be97baef237dce1f2511
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040841"
---
# <span data-ttu-id="16c2d-103"><a name="QRCODE">Funkce elektronického výkaznictví QRCODE</a></span><span class="sxs-lookup"><span data-stu-id="16c2d-103"><a name="QRCODE">QRCODE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16c2d-104">Funkce `QRCODE` vrátí hodnotu typu *kontejner*, která představuje kód rychlé odezvy (QR kód) pro zadaný řetězec v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="16c2d-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16c2d-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="16c2d-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="16c2d-106">Arguments</span></span>

<span data-ttu-id="16c2d-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="16c2d-107">`text`: *String*</span></span>

<span data-ttu-id="16c2d-108">Hodnota typu *řetězec*, která představuje původní text.</span><span class="sxs-lookup"><span data-stu-id="16c2d-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="16c2d-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="16c2d-109">Return values</span></span>

<span data-ttu-id="16c2d-110">*Kontejner*</span><span class="sxs-lookup"><span data-stu-id="16c2d-110">*Container*</span></span>

<span data-ttu-id="16c2d-111">Výsledný binární datový proud.</span><span class="sxs-lookup"><span data-stu-id="16c2d-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="16c2d-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="16c2d-112">Example</span></span>

<span data-ttu-id="16c2d-113">Můžete nakonfigurovat formát elektronického výkaznictví (ER) pro vygenerování odchozího dokumentu ve formátu Microsoft Office (sešity aplikace Excel nebo dokumenty aplikace Word) pomocí předdefinované šablony.</span><span class="sxs-lookup"><span data-stu-id="16c2d-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="16c2d-114">Tato šablona může obsahovat objekt **obrázku** (sešit aplikace Excel) nebo **ovládací prvek obsahu obrázku** (dokument aplikace Word) jako zástupný symbol pro obrázek kódu QR.</span><span class="sxs-lookup"><span data-stu-id="16c2d-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="16c2d-115">Do nakonfigurovaného formátu ER je třeba přidat prvek **buňky**, který se použije k vyplnění tohoto zástupného symbolu.</span><span class="sxs-lookup"><span data-stu-id="16c2d-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="16c2d-116">Chcete-li určit, jaké informace budou uloženy v kódu QR, musíte definovat vazbu pro tento prvek **buňky**.</span><span class="sxs-lookup"><span data-stu-id="16c2d-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="16c2d-117">Můžete například nakonfigurovat vazbu obsahující následující výraz:</span><span class="sxs-lookup"><span data-stu-id="16c2d-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="16c2d-118">Když spustíte konfigurovaný formát ER, textová hodnota pole **LabelText** ve zdroji dat **model.ListOfShelfLabels** bude použita ke generování obrázku kódu QR.</span><span class="sxs-lookup"><span data-stu-id="16c2d-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="16c2d-119">Tento obrázek nahradí zástupný symbol obrázku kódu QR v šabloně dokumentu použité ke generování odchozího dokumentu.</span><span class="sxs-lookup"><span data-stu-id="16c2d-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="16c2d-120">Když je obrázek vygenerovaného dokumentu naskenován, vrátí text, který byl převzat z pole **LabelText** ve zdroji dat **model.ListOfShelfLabels**.</span><span class="sxs-lookup"><span data-stu-id="16c2d-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="16c2d-121">Další informace viz [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="16c2d-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16c2d-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="16c2d-122">Additional resources</span></span>

[<span data-ttu-id="16c2d-123">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="16c2d-123">Text functions</span></span>](er-functions-category-text.md)
