---
title: Zobrazení transakcí vyrovnání pro východní Evropu
description: Toto téma obsahuje informace o transakcích vyrovnání na stránce pro zákazníky a dodavatele.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendTransPostingLog_RU
audience: Application User
ms.reviewer: kfend
ms.custom: 270544
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0034f38ebde15ae5a56632f6f59ec9a6f35a17a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236176"
---
# <a name="view-transactions-on-settlement-for-eastern-europe"></a><span data-ttu-id="d29c1-103">Zobrazení transakcí vyrovnání pro východní Evropu</span><span class="sxs-lookup"><span data-stu-id="d29c1-103">View transactions on settlement for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d29c1-104">Toto téma obsahuje informace o transakcích vyrovnání na stránce pro zákazníky a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="d29c1-104">This topic provides information about the Transactions on settlement page for customers and vendors.</span></span>

<span data-ttu-id="d29c1-105">Použijte stránku **Transakce u vyrovnání** stránce k zobrazení informací o složitých transakcích vyrovnání pro zákazníka nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="d29c1-105">Use the **Transactions on settlement** page to view information about complex settlement transactions for a customer or a vendor.</span></span> <span data-ttu-id="d29c1-106">Tato funkce je k dispozici pouze pro právnické osoby s primární adresu v Polsku, Litvě, Lotyšsku, Estonsku, České republice nebo Maďarsku.</span><span class="sxs-lookup"><span data-stu-id="d29c1-106">This feature is available only for legal entities that have their primary address in Lithuania, Latvia, Estonia, Czech Republic, Hungary, or Poland.</span></span> <span data-ttu-id="d29c1-107">Stránku **Transakce u vyrovnání** můžete najít v následujících umístěních:</span><span class="sxs-lookup"><span data-stu-id="d29c1-107">You can find the **Transactions on settlement** page at the following locations:</span></span>

-   <span data-ttu-id="d29c1-108">**Závazky** &gt; **Dodavatelé** &gt; **Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="d29c1-108">**Accounts payable** &gt; **Vendors** &gt; **All vendors**.</span></span> <span data-ttu-id="d29c1-109">V podokně akcí na kartě **Dodavatele** klikněte na **Transakce** &gt; **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="d29c1-109">On the Action Pane, on the **Vendor** tab, click **Transactions** &gt; **Transactions**.</span></span> <span data-ttu-id="d29c1-110">Na stránce **Transakce dodavatele** vyberte transakci a klepněte na tlačítko **Transakce u vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="d29c1-110">On the **Vendor transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>
-   <span data-ttu-id="d29c1-111">**Pohledávky** &gt; **Zákazníci** &gt; **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="d29c1-111">**Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span> <span data-ttu-id="d29c1-112">V podokně akcí na kartě **Zákazník** klikněte na **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="d29c1-112">On the Action Pane, on the **Customer** tab, click **Transactions**.</span></span> <span data-ttu-id="d29c1-113">Na stránce **Transakce zákazníka** vyberte transakci a klepněte na tlačítko **Transakce u vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="d29c1-113">On the **Customer transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>

<span data-ttu-id="d29c1-114">Informace týkající se vypořádání jsou zaznamenány a mohou být zobrazeny na stránce **Transakce u vyrovnání** pro transakce, které byly vytvořeny v následujících situacích:</span><span class="sxs-lookup"><span data-stu-id="d29c1-114">Settlement-related information is captured and can be shown on the **Transactions on settlement** page for transactions that were created in the following scenarios:</span></span>

-   <span data-ttu-id="d29c1-115">**Vyrovnání kurzových rozdílů** – vyrovnání faktury a platby generuje rozdíl realizovaného nebo nerealizovaného kurzového rozdílu.</span><span class="sxs-lookup"><span data-stu-id="d29c1-115">**Exchange adjustment** – Settlement of an invoice and a payment generates a realized or unrealized exchange rate difference.</span></span>
-   <span data-ttu-id="d29c1-116">**Změna profilu zaúčtování** – dvě položky, jako je faktura a dobropis, které mají různé účetní profily, jsou vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="d29c1-116">**Posting profile change** – Two entries, such as an invoice and a credit memo, that have different posting profiles are settled.</span></span>
-   <span data-ttu-id="d29c1-117">Záloha je převedena na platbu nebo platba je převedena na zálohu.</span><span class="sxs-lookup"><span data-stu-id="d29c1-117">A prepayment is converted to a payment, or a payment is converted to a prepayment.</span></span>
-   <span data-ttu-id="d29c1-118">**Platební sleva** – Faktura je vyrovnána s platbou, ze které byla stržena částka slevy.</span><span class="sxs-lookup"><span data-stu-id="d29c1-118">**Cash discount** – An invoice is settled with a payment that a discount amount has been deducted from.</span></span>
-   <span data-ttu-id="d29c1-119">**Haléřový rozdíl** – faktura je vyrovnána s platbou, která má mírně odlišnou částku než uvádí faktura.</span><span class="sxs-lookup"><span data-stu-id="d29c1-119">**Penny difference** – An invoice is settled with a payment that has a slightly different amount than the invoice.</span></span>
-   <span data-ttu-id="d29c1-120">**Podmíněné zaúčtování daně** – Faktura je vyrovnána s platbou, u které byla použita podmíněná daň.</span><span class="sxs-lookup"><span data-stu-id="d29c1-120">**Conditional tax posting** – An invoice is settled with a payment that conditional tax has been applied to.</span></span>
-   <span data-ttu-id="d29c1-121">**Vyrovnání mezi společnostmi** – mezipodniková funkce se používá k vyrovnání faktury s platbou z organizace.</span><span class="sxs-lookup"><span data-stu-id="d29c1-121">**Cross-company settlement** – Intercompany functionality is used to settle an invoice with a payment from an organization.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]