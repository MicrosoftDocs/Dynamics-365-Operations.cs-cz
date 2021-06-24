---
title: Vrácení produktů řízených sériovým číslem v POS
description: Toto téma popisuje možnosti pro ověřování serializovaných položek jako součást procesu vrácení v aplikaci Microsoft Dynamics 365 Commerce Point of Sale (POS).
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129797"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="1c0d9-103">Vrácení produktů řízených sériovým číslem v POS</span><span class="sxs-lookup"><span data-stu-id="1c0d9-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1c0d9-104">Toto téma popisuje možnosti pro ověřování serializovaných položek jako součást procesu vrácení v aplikaci Microsoft Dynamics 365 Commerce Point of Sale (POS).</span><span class="sxs-lookup"><span data-stu-id="1c0d9-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="1c0d9-105">Ve verzi Commerce verze 10.0.20 a novějších je k dispozici nová funkce s názvem **Sjednocené prostředí pro zpracování vrácení v POS**.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="1c0d9-106">Chcete-li během zpracování vratky objednávky v POS použít ověření sériového čísla, musíte tuto funkci zapnout.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="1c0d9-107">Informace o dalších schopnostech, které tato funkce poskytuje, když je zapnutá, najdete v tématu [Vytvoření vrácení v POS](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="1c0d9-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="1c0d9-108">Poté, co funkci zapnete, ji nelze vypnout.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="1c0d9-109">Možnosti pro ověření serializovaných vratek</span><span class="sxs-lookup"><span data-stu-id="1c0d9-109">Options for validating serialized returns</span></span>

<span data-ttu-id="1c0d9-110">Když je funkce **Sjednocené prostředí pro zpracování vrácení v POS** zapnutá, mohou organizace provádět ověření vracených položek řízených sériovým číslem prostřednictvím POS.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="1c0d9-111">Tato funkce může varovat uživatele, pokud se vracené sériové číslo liší od původního sériového čísla, které bylo prodáno.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="1c0d9-112">Ve verzi Commerce verze 10.0.20 a novějších je zpráva, kterou uživatelé obdrží, pouze varovnou zprávou.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="1c0d9-113">Uživatelé mohou pokračovat ve zpracování vratky i u sériového čísla, které se liší od původně prodaného sériového čísla.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="1c0d9-114">Chcete-li konfigurovat ověření sériového čísla pro organizaci po zapnutí funkce **Sjednocené prostředí pro zpracování vrácení v POS**, přejděte v centrále Commerce na nabídku **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="1c0d9-115">Na kartě **Zásoby** nastavte na záložce s náhledem **Operace skladových zásob** možnost **Povolit ověřování sériových čísel u vrácení POS** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="1c0d9-116">Zpracování vratek u serializovaných položek v POS</span><span class="sxs-lookup"><span data-stu-id="1c0d9-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="1c0d9-117">Když je možnost **Povolit ověřování sériových čísel u vrácení POS** nastavena na **Ano** a položka řízená sériovým číslem je vrácena přes POS, může uživatel zadat sériové číslo pro řádek vratky v podokně podrobností na stránce **Vratné produkty**.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="1c0d9-118">Pokud je zadané sériové číslo jiné než původní sériové číslo, které bylo prodáno v prodejní transakci, obdrží uživatel varovnou zprávu.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="1c0d9-119">Aplikace však nebrání uživateli pokračovat v odeslání vratky.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="1c0d9-120">V současné době POS podporuje ověřování sériových čísel pouze u řádků vrácení, kde původní objednané množství není větší než jedna.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="1c0d9-121">Pokud byl řádek původní prodejní objednávky vytvořen v kanálu nepatřícím do POS, a pokud je množství objednané pro serializovanou položku u daného řádku prodeje větší než jedna, nelze položku správně vrátit prostřednictvím POS.</span><span class="sxs-lookup"><span data-stu-id="1c0d9-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c0d9-122">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="1c0d9-122">Additional resources</span></span>

[<span data-ttu-id="1c0d9-123">Vytvoření vrácení v POS</span><span class="sxs-lookup"><span data-stu-id="1c0d9-123">Create returns in POS</span></span>](POS-returns.md)
