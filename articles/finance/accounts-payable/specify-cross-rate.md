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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a1463b9676e6b26543fd88607ca13b0ceb12be5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231559"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="9e381-103">Stanovení křížového kurzu</span><span class="sxs-lookup"><span data-stu-id="9e381-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e381-104">Toto téma popisuje účel křížového kurzu a zadání křížového kurzu při vyrovnání platby s fakturou.</span><span class="sxs-lookup"><span data-stu-id="9e381-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="9e381-105">Křížový kurz použijte, pokud platí následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="9e381-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="9e381-106">Má být vyrovnána platba pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="9e381-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="9e381-107">Řádek platby a řádek faktury používají různé měny.</span><span class="sxs-lookup"><span data-stu-id="9e381-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="9e381-108">Ani jedna měna není zúčtovací měna.</span><span class="sxs-lookup"><span data-stu-id="9e381-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="9e381-109">Křížový kurz není použit pro výpočet pro převod měny transakce platby na zúčtovací měnu platby.</span><span class="sxs-lookup"><span data-stu-id="9e381-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="9e381-110">Místo toho směnné kurzy z tabulky směnných kurzů jsou načteny pro výpočet hodnoty částky měny platební transakce platby a částky zúčtovací měny platby.</span><span class="sxs-lookup"><span data-stu-id="9e381-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="9e381-111">Například zúčtovací měna je USD, měna faktury je CAD a měna platby je EUR.</span><span class="sxs-lookup"><span data-stu-id="9e381-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="9e381-112">Křížový kurz umožňuje zadat směnný kurz pro převod přímo mezi CAD a EUR a není nutný převod prostřednictvím USD.</span><span class="sxs-lookup"><span data-stu-id="9e381-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="9e381-113">Pokud vyberete fakturu a primární platbu, můžete pro řádek faktury zadat křížovou měnu.</span><span class="sxs-lookup"><span data-stu-id="9e381-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="9e381-114">Termínem křížová měna se označuje směnný kurz mezi měnami pro transakce s ohledem na datum vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="9e381-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="9e381-115">Přejděte na jednu z následujících stránek:</span><span class="sxs-lookup"><span data-stu-id="9e381-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="9e381-116">**Pohledávky> Společné > Odběratelé > Všichni odběratelé**</span><span class="sxs-lookup"><span data-stu-id="9e381-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="9e381-117">**Závazky> Společné > Dodavatelé > Všichni dodavatelé**</span><span class="sxs-lookup"><span data-stu-id="9e381-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="9e381-118">**Zásobování a zdroje > Společné > Dodavatelé > Všichni dodavatelé.**</span><span class="sxs-lookup"><span data-stu-id="9e381-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="9e381-119">Vyberte odběratele nebo dodavatele, jejichž otevřené transakce mají být vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="9e381-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="9e381-120">Pro odběratele na stránce se seznamem **Všichni odběratelé** přejděte na **Shromáždit > Vyrovnat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="9e381-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="9e381-121">Pro dodavatele na stránce se seznamem **Všichni dodavatelé** přejděte na **Faktura > Vyrovnat otevřené transakce**.</span><span class="sxs-lookup"><span data-stu-id="9e381-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="9e381-122">Vyberte transakci, která je primární platbou, a klikněte na **Označit platbu**.</span><span class="sxs-lookup"><span data-stu-id="9e381-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="9e381-123">Bude zaškrtnuto políčko ve sloupci **Označit** a ve sloupci **Primární platba** bude zobrazena ikona pro informace.</span><span class="sxs-lookup"><span data-stu-id="9e381-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="9e381-124">V poli **Křížový kurz** zadejte směnný kurz mezi měnou faktury a měnou platby, s ohledem na datum vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="9e381-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]