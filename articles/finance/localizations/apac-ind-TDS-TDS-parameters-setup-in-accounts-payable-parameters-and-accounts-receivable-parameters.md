---
title: Nastavení parametrů TDS v závazcích a pohledávkách
description: Toto téma vysvětluje, jak nastavit parametry v závazcích a pohledávkách na podporu odpočtů daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023088"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="ea8d6-103">Nastavení parametrů TDS v závazcích a pohledávkách</span><span class="sxs-lookup"><span data-stu-id="ea8d6-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea8d6-104">Toto téma vysvětluje, jak nastavit parametry v závazcích a pohledávkách na podporu odpočtů daně odečtené u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="ea8d6-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="ea8d6-105">Přejděte do **Daň \> Nastavení \> Parametry \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="ea8d6-106">Na kartě **Aktualizace** vyberte **Aktualizovat řádky objednávky** k otevření dialogového okna **Aktualizovat řádky objednávky**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="ea8d6-107">V části **Skupina TDS** v poli **Aktualizace skupiny TDS** zadejte metodu, která se má použít k aktualizaci skupiny TDS na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="ea8d6-108">Toto nastavení se používá, když je skupina TDS aktualizována v záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="ea8d6-109">Existují tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-109">The following options are available:</span></span>

    - <span data-ttu-id="ea8d6-110">**Nikdy** – Skupina TDS není aktualizována na řádcích objednávky, když je aktualizována v záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="ea8d6-111">**Vždy** – Skupina TDS je automaticky aktualizována na řádcích objednávky, když je aktualizována v záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="ea8d6-112">**Výzva** – Uživatelé obdrží zprávu, která je vyzve k aktualizaci skupiny TDS na řádcích objednávky.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="ea8d6-113">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-113">Select **OK**.</span></span>

    <span data-ttu-id="ea8d6-114">[![Dialogové okno Aktualizovat řádky objednávky](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="ea8d6-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="ea8d6-115">Přejděte do **Daň \> Nastavení \> Parametry \> Parametry zakázek**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="ea8d6-116">Na kartě **Všeobecné** na pevné záložce **Rozdělit na základě informací o doručení** nastavte možnost **Příjem produktu** na **Ano** k zaúčtování a rozdělení příjemky produktu, která má různé doručovací adresy a čísla daňových účtů (TAN).</span><span class="sxs-lookup"><span data-stu-id="ea8d6-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="ea8d6-117">Pokud je tato možnost nastavena na **Ne**, nemůžete zaúčtovat nákupní dodací list, který má různé dodací adresy a TAN.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="ea8d6-118">Nastavte možnost **Faktura** na **Ano** k zaúčtování a rozdělení nákupní fakturu, která má různé dodací adresy a čísla TAN.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="ea8d6-119">[![Pevná záložka Rozdělit na základě informací o doručení](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="ea8d6-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="ea8d6-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-120">Close the page.</span></span>
