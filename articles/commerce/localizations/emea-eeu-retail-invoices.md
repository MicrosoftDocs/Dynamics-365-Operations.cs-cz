---
title: Faktury odběratele a vrácení prodejních objednávek ve východoevropských zemích
description: Toto téma popisuje způsob nastavení informací o fakturách odběratele a objednávkách prodejní vratky ve východoevropských zemích.
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a00a960142b0e3955c80d75f7963f4827209bf75
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004693"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="757ad-103">Faktury odběratele a vrácení prodejních objednávek ve východoevropských zemích</span><span class="sxs-lookup"><span data-stu-id="757ad-103">Customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="757ad-104">Toto téma popisuje způsob nastavení informací o fakturách odběratele a objednávkách prodejní vratky ve východoevropských zemích.</span><span class="sxs-lookup"><span data-stu-id="757ad-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="757ad-105">Můžete nastavit následující informace pro faktury odběratelů a objednávky prodejní vratky, které jsou generovány v Retail POS.</span><span class="sxs-lookup"><span data-stu-id="757ad-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="757ad-106">Můžete použít skupiny DPH ke zpracování vratek pomocí objednávek prodejní vratky.</span><span class="sxs-lookup"><span data-stu-id="757ad-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="757ad-107">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**.</span><span class="sxs-lookup"><span data-stu-id="757ad-107">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="757ad-108">Otevřete kartu **Zaúčtování \> Faktura** a potom nastavte **Použít skupinu prodejní daně pro vrácení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="757ad-108">Open the **Posting \> Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span>

    * <span data-ttu-id="757ad-109">K určení skupiny DPH pro vrácení, která jsou provedena zákazníkem, vyberte skupinu DPH na stránce **Odběratelé** na pevné záložce **Commerce** v poli **Skupina DPH pro vrácení**.</span><span class="sxs-lookup"><span data-stu-id="757ad-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Commerce** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="757ad-110">Pokud zaúčtujete objednávky prodejní vratky pro odběratele, řádek objednávky prodejní vratky bude aktualizován skupinou DPH pro vrácení, které je zadané ve formuláři **Odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="757ad-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
    * <span data-ttu-id="757ad-111">K určení skupiny DPH pro vrácení, která jsou provedena zákazníkem v Retail POS vyberte skupinu DPH na stránce **Obchody** na pevné záložce **Obecné** v poli **Skupina DPH pro vrácení**.</span><span class="sxs-lookup"><span data-stu-id="757ad-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="757ad-112">Pokud zaúčtujete objednávky prodejní vratky pro odběratele v obchodě, bude řádek objednávky prodejní vratky aktualizován skupinou DPH pro vrácení, která jsou zadaná na stránce **Obchody**.</span><span class="sxs-lookup"><span data-stu-id="757ad-112">When you post a return sales order for a customer of a  store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="757ad-113">Můžete použít datum zaúčtování faktury odběratele nebo objednávky prodejní vratky jako prodejní datum faktury nebo vratky, pokud faktura nebo vratka nemá výchozí datum prodeje.</span><span class="sxs-lookup"><span data-stu-id="757ad-113">You can use the posting date of a customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="757ad-114">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**.</span><span class="sxs-lookup"><span data-stu-id="757ad-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="757ad-115">Otevřete kartu **Zaúčtování \> Faktura** a potom nastavte **Použít datum zaúčtování jako datum prodeje** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="757ad-115">Open the **Posting \> Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>
- <span data-ttu-id="757ad-116">Můžete použít číselnou řadu poskytnutou finančními úřady k číslování faktur odběratele a objednávek prodejní vratky pro zákazníky v Lotyšsku a Litvě.</span><span class="sxs-lookup"><span data-stu-id="757ad-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span>

    * <span data-ttu-id="757ad-117">Přejděte na **Správa organizace \> Číselné řady \> Správa čítačů**.</span><span class="sxs-lookup"><span data-stu-id="757ad-117">Go to **Organization administration \> Number sequences \> Counters management**.</span></span> <span data-ttu-id="757ad-118">Musí existovat záznam, kde **Modul** = **Prodej** a **Typ** = **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="757ad-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>
    * <span data-ttu-id="757ad-119">Přejděte na **Správa organizace \> Číselné řady \> Nastavení číslování faktur**.</span><span class="sxs-lookup"><span data-stu-id="757ad-119">Go to **Organization administration \> Number sequences \> Invoice numbering setup**.</span></span> <span data-ttu-id="757ad-120">Zaškrtněte políčko **Commerce** pro pořadové číslo řádku, který se používá k číslování faktur odběratele.</span><span class="sxs-lookup"><span data-stu-id="757ad-120">Select the **Commerce** check box for the number sequence line that is used to number the customer invoices.</span></span>
