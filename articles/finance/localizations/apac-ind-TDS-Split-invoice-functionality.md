---
title: Funkce rozdělené faktury
description: Toto téma popisuje nastavení a funkce pro rozdělení faktur podle doručovací adresy a čísla daňového účtu (TAN).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023093"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="6fefc-103">Funkce rozdělené faktury</span><span class="sxs-lookup"><span data-stu-id="6fefc-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fefc-104">Toto téma popisuje nastavení a funkce pro rozdělení faktur podle doručovací adresy a čísla daňového účtu (TAN).</span><span class="sxs-lookup"><span data-stu-id="6fefc-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="6fefc-105">Na stránce **Parametry závazků** na kartě **Všeobecné** vyberte políčko **Příjem produktu** nebo **Faktura** pro zaúčtování a rozdělení dokladu o produktu nebo faktury, která má na serveru jiné doručovací adresy a čísla TAN na stránce **Nákupní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="6fefc-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="6fefc-106">Zaúčtovaná faktura bude poté rozdělena podle doručovací adresy a TAN.</span><span class="sxs-lookup"><span data-stu-id="6fefc-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="6fefc-107">Na kartě **Souhrnná aktualizace** na pevné záložce **Rozdělit na základě** v řádku **Informace o doručení** nastavte možnost **Potvrzení**, **Výdejka**, **Dodací list** nebo **Faktura** na **Ano** k zaúčtování a rozdělení potvrzení, výdejky, dodacího listu nebo faktury, kde jsou pro různé řádky faktury na stránce **Prodejní objednávka** definovány různé řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="6fefc-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="6fefc-108">Faktura bude nejprve rozdělena podle doručovací adresy a pak TAN.</span><span class="sxs-lookup"><span data-stu-id="6fefc-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="6fefc-109">Pokud nejsou žádné možnosti pro **Informace o doručení** nastaveny na **Ano**, bude faktura zaúčtována jako jedna faktura.</span><span class="sxs-lookup"><span data-stu-id="6fefc-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="6fefc-110">K rozdělení faktur nedojde.</span><span class="sxs-lookup"><span data-stu-id="6fefc-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="6fefc-111">Chcete-li rozdělit a zaúčtovat dodací list, kde řádky faktury mají různé dodací adresy a TAN, musíte nastavit možnost **Dodací list** pro **Informace o doručení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6fefc-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="6fefc-112">Chcete-li rozdělit a zaúčtovat fakturu, kde řádky faktury mají různé dodací adresy a TAN, musíte nastavit možnost **Faktura** pro **Informace o doručení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6fefc-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="6fefc-113">Chcete-li rozdělit a zaúčtovat fakturu, kde řádky faktury mají různé dodací adresy, ale stejné TAN, musíte nastavit možnost **Faktura** pro **Informace o doručení** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="6fefc-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="6fefc-114">Faktura bude rozdělena podle doručovací adresy.</span><span class="sxs-lookup"><span data-stu-id="6fefc-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="6fefc-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="6fefc-115">Example</span></span>

<span data-ttu-id="6fefc-116">V tomto příkladu možnost **Faktura** pro **Informace o doručení** je nastavena na **Ano** na kartě **Souhrnná aktualizace** stránky **Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="6fefc-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="6fefc-117">Zaúčtuje se nákupní faktura, která má následující nastavení pro doručovací adresy a TAN na řádcích:</span><span class="sxs-lookup"><span data-stu-id="6fefc-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="6fefc-118">**Řádek položky 1:** Dodací adresa 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="6fefc-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="6fefc-119">**Řádek položky 2:** Dodací adresa 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="6fefc-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="6fefc-120">**Řádek položky 3:** Dodací adresa 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="6fefc-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="6fefc-121">**Řádek položky 4:** Dodací adresa 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="6fefc-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="6fefc-122">V tomto případě je původní faktura rozdělena na dvě faktury a zaúčtována následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="6fefc-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="6fefc-123">Faktura 1 se zaúčtuje pro řádek 1 položky a řádek 2 položky, protože oba řádky mají stejnou doručovací adresu a TAN.</span><span class="sxs-lookup"><span data-stu-id="6fefc-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="6fefc-124">Faktura 2 se zaúčtuje za řádek 3 položky.</span><span class="sxs-lookup"><span data-stu-id="6fefc-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="6fefc-125">Faktura 3 se zaúčtuje za řádek 4 položky.</span><span class="sxs-lookup"><span data-stu-id="6fefc-125">Invoice 3 is posted for item line 4.</span></span>
