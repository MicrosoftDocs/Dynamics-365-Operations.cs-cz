---
title: "Stanovení křížového kurzu"
description: "Toto téma poskytuje informace o křížovém kurzu v aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="specify-the-cross-rate"></a><span data-ttu-id="8360c-103">Stanovení křížového kurzu</span><span class="sxs-lookup"><span data-stu-id="8360c-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8360c-104">Toto téma popisuje účel křížového kurzu a zadání křížového kurzu při vyrovnání platby s fakturou.</span><span class="sxs-lookup"><span data-stu-id="8360c-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="8360c-105">Křížový kurz použijte, pokud platí následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="8360c-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="8360c-106">Má být vyrovnána platba pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="8360c-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="8360c-107">Řádek platby a řádek faktury používají různé měny.</span><span class="sxs-lookup"><span data-stu-id="8360c-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="8360c-108">Ani jedna měna není zúčtovací měna.</span><span class="sxs-lookup"><span data-stu-id="8360c-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="8360c-109">Křížový kurz není použit pro výpočet pro převod měny transakce platby na zúčtovací měnu platby.</span><span class="sxs-lookup"><span data-stu-id="8360c-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="8360c-110">Místo toho směnné kurzy z tabulky směnných kurzů jsou načteny pro výpočet hodnoty částky měny platební transakce platby a částky zúčtovací měny platby.</span><span class="sxs-lookup"><span data-stu-id="8360c-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="8360c-111">Například zúčtovací měna je USD, měna faktury je CAD a měna platby je EUR.</span><span class="sxs-lookup"><span data-stu-id="8360c-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="8360c-112">Křížový kurz umožňuje zadat směnný kurz pro převod přímo mezi CAD a EUR a není nutný převod prostřednictvím USD.</span><span class="sxs-lookup"><span data-stu-id="8360c-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="8360c-113">Pokud vyberete fakturu a primární platbu, můžete pro řádek faktury zadat křížovou měnu.</span><span class="sxs-lookup"><span data-stu-id="8360c-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="8360c-114">Termínem křížová měna se označuje směnný kurz mezi měnami pro transakce s ohledem na datum vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="8360c-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="8360c-115">Přejděte na jednu z následujících stránek:</span><span class="sxs-lookup"><span data-stu-id="8360c-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="8360c-116">**Pohledávky> Společné > Odběratelé > Všichni odběratelé**</span><span class="sxs-lookup"><span data-stu-id="8360c-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="8360c-117">**Závazky> Společné > Dodavatelé > Všichni dodavatelé**</span><span class="sxs-lookup"><span data-stu-id="8360c-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="8360c-118">**Zásobování a zdroje > Společné > Dodavatelé > Všichni dodavatelé.**</span><span class="sxs-lookup"><span data-stu-id="8360c-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="8360c-119">Vyberte odběratele nebo dodavatele, jejichž otevřené transakce mají být vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="8360c-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="8360c-120">Pro odběratele na stránce se seznamem **Všichni odběratelé** přejděte na **Shromáždit > Vyrovnat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="8360c-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="8360c-121">Pro dodavatele na stránce se seznamem **Všichni dodavatelé** přejděte na **Faktura > Vyrovnat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="8360c-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="8360c-122">Vyberte transakci, která je primární platbou, a klikněte na **Označit platbu**.</span><span class="sxs-lookup"><span data-stu-id="8360c-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="8360c-123">Bude zaškrtnuto políčko ve sloupci **Označit** a ve sloupci **Primární platba** bude zobrazena ikona pro informace.</span><span class="sxs-lookup"><span data-stu-id="8360c-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="8360c-124">V poli **Křížový kurz** zadejte směnný kurz mezi měnou faktury a měnou platby, s ohledem na datum vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="8360c-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 

