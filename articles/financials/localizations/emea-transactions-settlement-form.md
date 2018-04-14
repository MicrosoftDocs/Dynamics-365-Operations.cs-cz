---
title: "Zobrazení transakcí vyrovnání pro východní Evropu"
description: "Toto téma obsahuje informace o transakcích vyrovnání na stránce pro zákazníky a dodavatele."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustVendTransPostingLog_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 270544
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e2972d06346533659dfc26ac243dc57ec5e0f6fb
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="view-transactions-on-settlement-for-eastern-europe"></a><span data-ttu-id="82371-103">Zobrazení transakcí vyrovnání pro východní Evropu</span><span class="sxs-lookup"><span data-stu-id="82371-103">View transactions on settlement for Eastern Europe</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="82371-104">Toto téma obsahuje informace o transakcích vyrovnání na stránce pro zákazníky a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="82371-104">This topic provides information about the Transactions on settlement page for customers and vendors.</span></span>

<span data-ttu-id="82371-105">Použijte stránku **Transakce u vyrovnání** stránce k zobrazení informací o složitých transakcích vyrovnání pro zákazníka nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="82371-105">Use the **Transactions on settlement** page to view information about complex settlement transactions for a customer or a vendor.</span></span> <span data-ttu-id="82371-106">Tato funkce je k dispozici pouze pro právnické osoby s primární adresu v Polsku, Litvě, Lotyšsku, Estonsku, České republice nebo Maďarsku.</span><span class="sxs-lookup"><span data-stu-id="82371-106">This feature is available only for legal entities that have their primary address in Lithuania, Latvia, Estonia, Czech Republic, Hungary, or Poland.</span></span> <span data-ttu-id="82371-107">Stránku **Transakce u vyrovnání** můžete najít v následujících umístěních:</span><span class="sxs-lookup"><span data-stu-id="82371-107">You can find the **Transactions on settlement** page at the following locations:</span></span>

-   <span data-ttu-id="82371-108">**Závazky** &gt; **Dodavatelé** &gt; **Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="82371-108">**Accounts payable** &gt; **Vendors** &gt; **All vendors**.</span></span> <span data-ttu-id="82371-109">V podokně akcí na kartě **Dodavatele** klikněte na **Transakce** &gt; **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="82371-109">On the Action Pane, on the **Vendor** tab, click **Transactions** &gt; **Transactions**.</span></span> <span data-ttu-id="82371-110">Na stránce **Transakce dodavatele** vyberte transakci a klepněte na tlačítko **Transakce u vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="82371-110">On the **Vendor transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>
-   <span data-ttu-id="82371-111">**Pohledávky** &gt; **Zákazníci** &gt; **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="82371-111">**Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span> <span data-ttu-id="82371-112">V podokně akcí na kartě **Zákazník** klikněte na **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="82371-112">On the Action Pane, on the **Customer** tab, click **Transactions**.</span></span> <span data-ttu-id="82371-113">Na stránce **Transakce zákazníka** vyberte transakci a klepněte na tlačítko **Transakce u vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="82371-113">On the **Customer transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>

<span data-ttu-id="82371-114">Informace týkající se vypořádání jsou zaznamenány a mohou být zobrazeny na stránce **Transakce u vyrovnání** pro transakce, které byly vytvořeny v následujících situacích:</span><span class="sxs-lookup"><span data-stu-id="82371-114">Settlement-related information is captured and can be shown on the **Transactions on settlement** page for transactions that were created in the following scenarios:</span></span>

-   <span data-ttu-id="82371-115">**Vyrovnání kurzových rozdílů** – vyrovnání faktury a platby generuje rozdíl realizovaného nebo nerealizovaného kurzového rozdílu.</span><span class="sxs-lookup"><span data-stu-id="82371-115">**Exchange adjustment** – Settlement of an invoice and a payment generates a realized or unrealized exchange rate difference.</span></span>
-   <span data-ttu-id="82371-116">**Změna profilu zaúčtování** – dvě položky, jako je faktura a dobropis, které mají různé účetní profily, jsou vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="82371-116">**Posting profile change** – Two entries, such as an invoice and a credit memo, that have different posting profiles are settled.</span></span>
-   <span data-ttu-id="82371-117">Záloha je převedena na platbu nebo platba je převedena na zálohu.</span><span class="sxs-lookup"><span data-stu-id="82371-117">A prepayment is converted to a payment, or a payment is converted to a prepayment.</span></span>
-   <span data-ttu-id="82371-118">**Platební sleva** – Faktura je vyrovnána s platbou, ze které byla stržena částka slevy.</span><span class="sxs-lookup"><span data-stu-id="82371-118">**Cash discount** – An invoice is settled with a payment that a discount amount has been deducted from.</span></span>
-   <span data-ttu-id="82371-119">**Haléřový rozdíl** – faktura je vyrovnána s platbou, která má mírně odlišnou částku než uvádí faktura.</span><span class="sxs-lookup"><span data-stu-id="82371-119">**Penny difference** – An invoice is settled with a payment that has a slightly different amount than the invoice.</span></span>
-   <span data-ttu-id="82371-120">**Podmíněné zaúčtování daně** – Faktura je vyrovnána s platbou, u které byla použita podmíněná daň.</span><span class="sxs-lookup"><span data-stu-id="82371-120">**Conditional tax posting** – An invoice is settled with a payment that conditional tax has been applied to.</span></span>
-   <span data-ttu-id="82371-121">**Vyrovnání mezi společnostmi** – mezipodniková funkce se používá k vyrovnání faktury s platbou z organizace.</span><span class="sxs-lookup"><span data-stu-id="82371-121">**Cross-company settlement** – Intercompany functionality is used to settle an invoice with a payment from an organization.</span></span>





