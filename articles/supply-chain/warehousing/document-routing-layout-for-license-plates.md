---
title: Rozvržení směrování dokumentu pro popisky poznávací značky
description: V tomto tématu je popsán způsob použití metod formátování k tisku hodnot na štítcích.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 6b5bf6815f225dcca8f9e89e2c85942ce8a2ccd7
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907980"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="4c152-103">Rozvržení směrování dokumentu pro popisky poznávací značky</span><span class="sxs-lookup"><span data-stu-id="4c152-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4c152-104">Rozvržení směrování dokumentu definuje rozvržení popisků řidičských průkazů a dat, která jsou na nich vytištěna.</span><span class="sxs-lookup"><span data-stu-id="4c152-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="4c152-105">Body aktivace tisku se nastavují při nastavení položek nabídky mobilního zařízení a pracovních šablon.</span><span class="sxs-lookup"><span data-stu-id="4c152-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="4c152-106">V obvyklém scénáři pracovník příjmu ve skladu vytiskněte štítky registračních značek ihned po záznamu obsahu palet, které přicházejí do oblasti příjmu.</span><span class="sxs-lookup"><span data-stu-id="4c152-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="4c152-107">Fyzické štítky se použijí na palety.</span><span class="sxs-lookup"><span data-stu-id="4c152-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="4c152-108">Poté je lze použít k ověření v rámci procesu zaskladnění a následných operací odchozího vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="4c152-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="4c152-109">Můžete tisknout velmi složité štítky za předpokladu, že tiskové zařízení může interpretovat text, který mu byl odeslán.</span><span class="sxs-lookup"><span data-stu-id="4c152-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="4c152-110">Například rozložení Zebra Programming Language (ZPL), které obsahuje čárový kód, může vypadat podobně jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="4c152-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="4c152-111">V rámci procesu tisku štítků bude text `$LicensePlateId$` v tomto příkladu nahrazen datovou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="4c152-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="4c152-112">Chcete-li zobrazit hodnoty, které budou vytištěny, přejděte na **Řízení skladu \> Dotazy a sestavy \> Štítky registračních značek**.</span><span class="sxs-lookup"><span data-stu-id="4c152-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="4c152-113">Několik široce dostupných nástrojů pro generování štítků vám může pomoci formátovat text pro rozvržení štítků.</span><span class="sxs-lookup"><span data-stu-id="4c152-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="4c152-114">Mnohé z těchto nástrojů podporují `$FieldName$` formát.</span><span class="sxs-lookup"><span data-stu-id="4c152-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="4c152-115">Kromě toho Microsoft Dynamics 365 Supply Chain Management používá speciální logiku formátování jako součást mapování polí pro rozložení směrování dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4c152-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="4c152-116">Zapnutí této funkce ve vašem systému</span><span class="sxs-lookup"><span data-stu-id="4c152-116">Turn on this feature for your system</span></span>

<span data-ttu-id="4c152-117">Pokud váš systém ještě neobsahuje funkce popsané v tomto tématu, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Vylepšené rozvržení popisků poznávacích značek*.</span><span class="sxs-lookup"><span data-stu-id="4c152-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="4c152-118">Vlastní formáty čísel</span><span class="sxs-lookup"><span data-stu-id="4c152-118">Custom number formats</span></span>

<span data-ttu-id="4c152-119">Formátování hodnot číselných polí, které jsou vytištěny pomocí kódů s následujícím formátem, lze přizpůsobit.</span><span class="sxs-lookup"><span data-stu-id="4c152-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="4c152-120">Zde je vysvětlení tohoto formátu:</span><span class="sxs-lookup"><span data-stu-id="4c152-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="4c152-121">`FieldName` je název datového pole (například **množství**).</span><span class="sxs-lookup"><span data-stu-id="4c152-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="4c152-122">`FormatString` definuje způsob tisku dat.</span><span class="sxs-lookup"><span data-stu-id="4c152-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="4c152-123">Následující příklady ukazují, jak lze upravit pole pracovní množství (**množství**):</span><span class="sxs-lookup"><span data-stu-id="4c152-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="4c152-124">Chcete-li vždy zobrazit čtyři číslice (pomocí nul jako zástupné symboly), použijte `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="4c152-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="4c152-125">Pokud je například množství 10, štítek zobrazí "0010".</span><span class="sxs-lookup"><span data-stu-id="4c152-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="4c152-126">Chcete-li vždy zobrazit dvě desetinná místa, použijte možnost `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="4c152-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="4c152-127">Pokud je například množství 10, štítek zobrazí "10.00".</span><span class="sxs-lookup"><span data-stu-id="4c152-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="4c152-128">Úplný seznam dostupných formátovacích řetězců čísel naleznete v tématu [Vlastní číselné formátovací řetězce](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="4c152-128">For a complete list of the available number format strings, see [Custom numeric format strings](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="4c152-129">Formáty vlastních řetězců</span><span class="sxs-lookup"><span data-stu-id="4c152-129">Custom string formats</span></span>

<span data-ttu-id="4c152-130">První znaky řetězce můžete odebrat pomocí následujícího pole a kódu formátu.</span><span class="sxs-lookup"><span data-stu-id="4c152-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="4c152-131">Zde určuje `#` počet znaků, které mají být přeskočeny.</span><span class="sxs-lookup"><span data-stu-id="4c152-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="4c152-132">Chcete-li například vytisknout sériové číslo kontejneru (SSCC), který neobsahuje první dva znaky, použijte možnost `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="4c152-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="4c152-133">V takovém případě bude číslo registrační značky 0011111111111222221 vytisknuto jako 11111111111222221.</span><span class="sxs-lookup"><span data-stu-id="4c152-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="4c152-134">Vlastní formáty data a času</span><span class="sxs-lookup"><span data-stu-id="4c152-134">Custom date/time formats</span></span>

<span data-ttu-id="4c152-135">V následujícím příkladu je ukázáno, jak lze ovládat formát používaný k tisku dat.</span><span class="sxs-lookup"><span data-stu-id="4c152-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="4c152-136">V tomto příkladu bude datum 30. dubna 2020 vytisknuto jako "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="4c152-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="4c152-137">Úplný seznam dostupných formátů data/času naleznete v tématu [Vlastní formátovací řetězce data/času](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="4c152-137">For a complete list of the available date/time formats, see [Custom date and time format strings](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="4c152-138">Tisk jednotlivých řádků z víceřádkových dat</span><span class="sxs-lookup"><span data-stu-id="4c152-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="4c152-139">Obsahuje-li datové pole více řádků (tj. řádků oddělených zalomením řádků), můžete vytisknout jednotlivé řádky s použitím následujícího formátu.</span><span class="sxs-lookup"><span data-stu-id="4c152-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="4c152-140">Zde `#` je číslo řádku, který chcete vytisknout.</span><span class="sxs-lookup"><span data-stu-id="4c152-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="4c152-141">(Pro první řádek použijte 1.)</span><span class="sxs-lookup"><span data-stu-id="4c152-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="4c152-142">Váš systém má například pole `AdditionalAddress`, ve kterém je uložena následující víceřádková adresa:</span><span class="sxs-lookup"><span data-stu-id="4c152-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="4c152-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="4c152-143">Contoso Inc.</span></span>  
<span data-ttu-id="4c152-144">Název ulice 123</span><span class="sxs-lookup"><span data-stu-id="4c152-144">123 Street Name</span></span>  
<span data-ttu-id="4c152-145">Některé město, některý stát</span><span class="sxs-lookup"><span data-stu-id="4c152-145">Some City, Some State</span></span>

<span data-ttu-id="4c152-146">Tuto adresu lze po jednotlivých řádcích vytisknout pomocí následujících kódů.</span><span class="sxs-lookup"><span data-stu-id="4c152-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="4c152-147">Kód</span><span class="sxs-lookup"><span data-stu-id="4c152-147">Code</span></span> | <span data-ttu-id="4c152-148">Text vytištěný</span><span class="sxs-lookup"><span data-stu-id="4c152-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="4c152-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="4c152-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="4c152-150">Název ulice 123</span><span class="sxs-lookup"><span data-stu-id="4c152-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="4c152-151">Některé město, některý stát</span><span class="sxs-lookup"><span data-stu-id="4c152-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="4c152-152">Tisk a formátování z metody zobrazení</span><span class="sxs-lookup"><span data-stu-id="4c152-152">Print and format from a display method</span></span>

<span data-ttu-id="4c152-153">Můžete tisknout z metody zobrazení v následujícím formátu.</span><span class="sxs-lookup"><span data-stu-id="4c152-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="4c152-154">Tento formát lze kombinovat s jinými typy, které byly popsány dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="4c152-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="4c152-155">Například máte pojmenovanou metodu zobrazení `DisplayListOfItemsNumbers()` a chcete vytisknout číslo první položky této metody.</span><span class="sxs-lookup"><span data-stu-id="4c152-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="4c152-156">V takovém případě můžete použít následující kód.</span><span class="sxs-lookup"><span data-stu-id="4c152-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="4c152-157">Další informace o tisku štítků</span><span class="sxs-lookup"><span data-stu-id="4c152-157">More information about how to print labels</span></span>

<span data-ttu-id="4c152-158">Další informace o nastavení a tisku štítků naleznete v tématu [Povolení tisku štítků registračních značek](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="4c152-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]