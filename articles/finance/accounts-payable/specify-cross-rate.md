---
title: Stanovení křížového kurzu
description: Toto téma obsahuje obecné informace o křížených sazbách v aplikaci Microsoft Dynamics 365 Finance.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146794557a3a6ba1801598fe6b814e209d9f5fc6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441000"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="71614-103">Stanovení křížového kurzu</span><span class="sxs-lookup"><span data-stu-id="71614-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71614-104">Toto téma popisuje účel křížového kurzu a zadání křížového kurzu při vyrovnání platby s fakturou.</span><span class="sxs-lookup"><span data-stu-id="71614-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="71614-105">Křížový kurz použijte, pokud platí následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="71614-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="71614-106">Má být vyrovnána platba pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="71614-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="71614-107">Řádek platby a řádek faktury používají různé měny.</span><span class="sxs-lookup"><span data-stu-id="71614-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="71614-108">Ani jedna měna není zúčtovací měna.</span><span class="sxs-lookup"><span data-stu-id="71614-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="71614-109">Křížový kurz není použit pro výpočet pro převod měny transakce platby na zúčtovací měnu platby.</span><span class="sxs-lookup"><span data-stu-id="71614-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="71614-110">Místo toho směnné kurzy z tabulky směnných kurzů jsou načteny pro výpočet hodnoty částky měny platební transakce platby a částky zúčtovací měny platby.</span><span class="sxs-lookup"><span data-stu-id="71614-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="71614-111">Například zúčtovací měna je USD, měna faktury je CAD a měna platby je EUR.</span><span class="sxs-lookup"><span data-stu-id="71614-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="71614-112">Křížový kurz umožňuje zadat směnný kurz pro převod přímo mezi CAD a EUR a není nutný převod prostřednictvím USD.</span><span class="sxs-lookup"><span data-stu-id="71614-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="71614-113">Pokud vyberete fakturu a primární platbu, můžete pro řádek faktury zadat křížovou měnu.</span><span class="sxs-lookup"><span data-stu-id="71614-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="71614-114">Termínem křížová měna se označuje směnný kurz mezi měnami pro transakce s ohledem na datum vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="71614-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="71614-115">Přejděte na jednu z následujících stránek:</span><span class="sxs-lookup"><span data-stu-id="71614-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="71614-116">**Pohledávky> Společné > Odběratelé > Všichni odběratelé**</span><span class="sxs-lookup"><span data-stu-id="71614-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="71614-117">**Závazky> Společné > Dodavatelé > Všichni dodavatelé**</span><span class="sxs-lookup"><span data-stu-id="71614-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="71614-118">**Zásobování a zdroje > Společné > Dodavatelé > Všichni dodavatelé.**</span><span class="sxs-lookup"><span data-stu-id="71614-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="71614-119">Vyberte odběratele nebo dodavatele, jejichž otevřené transakce mají být vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="71614-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="71614-120">Pro odběratele na stránce se seznamem **Všichni odběratelé** přejděte na **Shromáždit > Vyrovnat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="71614-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="71614-121">Pro dodavatele na stránce se seznamem **Všichni dodavatelé** přejděte na **Faktura > Vyrovnat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="71614-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="71614-122">Vyberte transakci, která je primární platbou, a klikněte na **Označit platbu**.</span><span class="sxs-lookup"><span data-stu-id="71614-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="71614-123">Bude zaškrtnuto políčko ve sloupci **Označit** a ve sloupci **Primární platba** bude zobrazena ikona pro informace.</span><span class="sxs-lookup"><span data-stu-id="71614-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="71614-124">V poli **Křížový kurz** zadejte směnný kurz mezi měnou faktury a měnou platby, s ohledem na datum vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="71614-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
