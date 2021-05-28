---
title: Aktualizace čísel a dat certifikátu pro transakce TDS
description: Toto téma vysvětluje, jak aktualizovat čísla a data vratných certifikátů, které byly zaznamenány pro účet dodavatele, zákazníka hlavní knihy a pro daň odečtenou u zdroje (TDS).
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023084"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="86738-103">Aktualizace čísel a dat certifikátu pro transakce TDS</span><span class="sxs-lookup"><span data-stu-id="86738-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86738-104">Toto téma vysvětluje, jak aktualizovat čísla a data vratných certifikátů, které byly zaznamenány pro účet dodavatele, zákazníka hlavní knihy a pro daň odečtenou u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="86738-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="86738-105">Certifikáty pro transakce TDS si můžete prohlédnout na stránce **Vratné certifikáty**.</span><span class="sxs-lookup"><span data-stu-id="86738-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="86738-106">Certifikáty můžete aktualizovat pomocí stránky **Aktualizovat certifikáty** .</span><span class="sxs-lookup"><span data-stu-id="86738-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="86738-107">Podle těchto pokynů aktualizujete čísla a data certifikátu pro transakci TDS.</span><span class="sxs-lookup"><span data-stu-id="86738-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="86738-108">Přejděte do nabídky **Daň \> Přiznání \> Srážková daň \> Aktualizovat certifikát**.</span><span class="sxs-lookup"><span data-stu-id="86738-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="86738-109">[![Stránka Aktualizovat certifikát](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="86738-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="86738-110">Na stránce **Aktualizovat certifikát** v části **Vybrat** v poli **Typ daně** vyberte **TDS**.</span><span class="sxs-lookup"><span data-stu-id="86738-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="86738-111">V poli **Číslo certifikátu** vyberte číslo certifikátu TDS zákazníka nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="86738-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86738-112">Pole **Číslo certifikátu** uvádí pouze čísla certifikátů TDS, pro která je políčko **Uzavřeno** nezaškrtnuté na stránce **Vratné certifikáty**.</span><span class="sxs-lookup"><span data-stu-id="86738-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="86738-113">Pole **Datum certifikátu** zobrazuje datum certifikátu.</span><span class="sxs-lookup"><span data-stu-id="86738-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="86738-114">Pole **Typ účtu** zobrazuje typ účtu, pro který je přijato číslo certifikátu TDS, a pole **Název** zobrazuje název účtu.</span><span class="sxs-lookup"><span data-stu-id="86738-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="86738-115">V polích **Od data** a **Do data** vyberte počáteční a koncová data období, pro která se mají zobrazit transakce TDS.</span><span class="sxs-lookup"><span data-stu-id="86738-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="86738-116">Vyberte **Zobrazit data** k zobrazení transakcí TDS, které byly zaúčtovány během vybraného období.</span><span class="sxs-lookup"><span data-stu-id="86738-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="86738-117">Na kartě **Přehled**, mřížka v horním podokně zobrazuje následující informace o každé transakci TDS, která byla zaúčtována pro dodavatele nebo zákazníka během vybraného období:</span><span class="sxs-lookup"><span data-stu-id="86738-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="86738-118">**Doklad** – Zobrazí pro danou transakci TDS číslo dokladu.</span><span class="sxs-lookup"><span data-stu-id="86738-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="86738-119">**Datum** – datum transakce TDS.</span><span class="sxs-lookup"><span data-stu-id="86738-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="86738-120">**Částka** – Částka faktury, podle které byla TDS vypočítána.</span><span class="sxs-lookup"><span data-stu-id="86738-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="86738-121">**Výše daně** – Částka daně TDS, která byla vypočítána pro transakci.</span><span class="sxs-lookup"><span data-stu-id="86738-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="86738-122">Chcete-li přesunout konkrétní transakce TDS z horní mřížky do dolní mřížky, vyberte transakce a poté vyberte **Zahrnout**.</span><span class="sxs-lookup"><span data-stu-id="86738-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="86738-123">Případně vyberte **Zahrnout vše** a přesuňte všechny transakce TDS z horní mřížky do spodní mřížky.</span><span class="sxs-lookup"><span data-stu-id="86738-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="86738-124">Chcete-li přesunout konkrétní transakce TDS nebo všechny transakce TDS ze spodní mřížky do horní mřížky, použijte tlačítka **Vyloučit** nebo **Vyloučit vše**.</span><span class="sxs-lookup"><span data-stu-id="86738-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="86738-125">Vyberte **Aktualizovat** k aktualizaci polí **Číslo certifikátu** a **Datum certifikátu** pro transakce TDS ve spodní mřížce.</span><span class="sxs-lookup"><span data-stu-id="86738-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="86738-126">Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Vratný certifikát** a vyberte **Poptávka** pro zobrazení aktualizovaných řádků transakcí, které mají na certifikátu nová čísla certifikátů na stránce **Transakce s certifikáty**.</span><span class="sxs-lookup"><span data-stu-id="86738-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="86738-127">[![Stránka Transakce s certifikátem](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="86738-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
