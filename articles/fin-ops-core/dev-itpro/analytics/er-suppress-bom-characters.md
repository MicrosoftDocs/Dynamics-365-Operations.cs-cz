---
title: Návrh konfigurací ER k potlačení znaků kusovníku ve vygenerovaných souborech
description: Toto téma vysvětluje, jak nakonfigurovat formát elektronického výkaznictví (ER) pro generování sestav, které potlačují znaky značka pořadí bajtů (BOM).
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ada93c0192aadac70c38c8c8c4f3af86ff6fc3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893269"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="6ad2d-103">Návrh konfigurací ER k potlačení znaků kusovníku ve vygenerovaných souborech</span><span class="sxs-lookup"><span data-stu-id="6ad2d-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ad2d-104">Můžete navrhnout [řešení](general-electronic-reporting.md) [pro formát elektronického výkaznictví (ER)](er-quick-start1-new-solution.md) ke generování odchozích dokumentů.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="6ad2d-105">Chcete-li generovat dokumenty jako textové nebo XML soubory, musí řešení obsahovat [konfiguraci](general-electronic-reporting.md#Configuration) ER, která obsahuje komponentu [formátu](general-electronic-reporting.md#FormatComponentOutbound) ER.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="6ad2d-106">Chcete-li určit [kódování znaků](/windows/win32/intl/character-sets), které představuje sadu znaků v generovaných souborech, musí formát ER obsahovat prvek formátu **Běžný\\Soubor**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-106">To specify the [character encoding](/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="6ad2d-107">Chcete-li nakonfigurovat komponentu formátu ER, musíte otevřít [rámcovou](general-electronic-reporting.md#component-versioning) verzi konfigurace ER v návrháři formátu ER a přidat prvek **Vlastní\\Soubor**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="6ad2d-108">V poli **Kódování** zadejte kódování odchozích souborů generovaných za běhu pomocí této komponenty.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="6ad2d-109">Pokud formát obsahuje nesprávný název kódování, dojde k chybě, když uložíte změny v nastavení formátu.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Přidání kořenového prvku a polí na stránce Návrhář formátu](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="6ad2d-111">Pokud jako kódování zadáte **UTF-8**, **UTF-16**, nebo **UTF-32**, zpřístupní se možnost **Potlačit znaky BOM**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="6ad2d-112">Tuto možnost nastavte na **Ano**, pokud chcete potlačit [znaky pořadí bajtů (BOM)](/globalization/encoding/byte-order-mark) v odchozích souborech, které jsou generovány za běhu, když je spuštěn upravitelný formát ER.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="6ad2d-113">Ponecháte-li pole **Kódování** prázdné, použije se výchozí kódování **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Nastavení možnosti Potlačit znaky BOM na stránce Návrhář formátů](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="6ad2d-115">Chcete-li zkontrolovat funkčnost za běhu, proveďte příslušný postup.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="6ad2d-116">Například proveďte kroky v tématu [Odložit provedení prvků XML ve formátech ER](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="6ad2d-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="6ad2d-117">Po dokončení kroků v části [Úprava formátu tak, aby byl výpočet založen na generovaném výstupu](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) tohoto tématu, postupujte podle těchto dalších kroků.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="6ad2d-118">Zadejte kódování UTF:</span><span class="sxs-lookup"><span data-stu-id="6ad2d-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="6ad2d-119">vyberte prvek **Report** typu **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="6ad2d-120">Do pole **Kódování** zadejte kódování **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="6ad2d-121">Vygenerujte soubor XML, který obsahuje znak BOM:</span><span class="sxs-lookup"><span data-stu-id="6ad2d-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="6ad2d-122">Nastavte možnost **Potlačit znaky BOM** na **Ne**, pokud chcete zahrnout znaky BOM do vygenerovaných souborů XML.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="6ad2d-123">Proveďte kroky v části [Odložit provedení souhrnného prvku XML tak, aby se použil vypočítaný součet](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) tématu [Odložení provedení prvků XML ve formátech ER](er-defer-xml-element.md) a uložte vygenerovaný soubor jako **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="6ad2d-124">Vygenerujte soubor XML, který neobsahuje znak BOM:</span><span class="sxs-lookup"><span data-stu-id="6ad2d-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="6ad2d-125">Nastavte možnost **Potlačit znaky BOM** na **Ano**, pokud chcete potlačit znaky BOM do vygenerovaných souborů XML.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="6ad2d-126">Proveďte kroky v části [Odložit provedení souhrnného prvku XML tak, aby se použil vypočítaný součet](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) tématu [Odložení provedení prvků XML ve formátech ER](er-defer-xml-element.md) a uložte vygenerovaný soubor jako **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="6ad2d-127">V nástroji pro porovnávání souborů porovnejte vygenerované soubory.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="6ad2d-128">První rozdíl, kterého si všimnete, je v záhlaví souboru.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="6ad2d-129">Soubor SampleXmlReport.xml obsahuje znak BOM, kdežto soubor SampleXmlReport (1) .xml nikoli.</span><span class="sxs-lookup"><span data-stu-id="6ad2d-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Porovnávání generovaných souborů pomocí nástroje pro porovnání souborů](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="6ad2d-131">Viz také</span><span class="sxs-lookup"><span data-stu-id="6ad2d-131">See also</span></span>

- [<span data-ttu-id="6ad2d-132">Odložení provádění prvků XML ve formátech elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="6ad2d-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]