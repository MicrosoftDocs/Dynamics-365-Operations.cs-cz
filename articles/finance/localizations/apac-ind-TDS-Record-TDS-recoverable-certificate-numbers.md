---
title: Zázname čísla vratných certifikátů TDS
description: Toto téma vysvětluje, jak pomocí stránky Vratné certifikáty zaznamenat čísla a data certifikátů pro certifikáty TDS (daň odečtená u zdroje), které jsou přijímány pro konkrétního dodavatele, zákazníka nebo hlavní knihu.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023074"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="5b4bd-103">Zázname čísla vratných certifikátů TDS</span><span class="sxs-lookup"><span data-stu-id="5b4bd-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b4bd-104">Toto téma vysvětluje, jak pomocí stránky **Vratné certifikáty** zaznamenat čísla a data certifikátů pro certifikáty TDS (daň odečtená u zdroje), které jsou přijímány pro konkrétního dodavatele, zákazníka nebo hlavní knihu.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="5b4bd-105">Chcete-li aktualizovat čísla a data certifikátu TDS, která jsou zaznamenána pro transakce TDS na této stránce, použijte stránku **Aktualizovat certifikát** (**Hlavní kniha \> Periodické \> Srážková daň \> Aktualizovat certifikát**).</span><span class="sxs-lookup"><span data-stu-id="5b4bd-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="5b4bd-106">Po dokončení aktualizace čísel certifikátů TDS je zavřete.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="5b4bd-107">Podle těchto pokynů zaznamenáte čísla a data certifikátu TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="5b4bd-108">Přejděte na **Daň \> Nepřímá daň \> Srážková daň \> Vratné certifikáty**.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="5b4bd-109">[![Stránka Vratné certifikáty](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="5b4bd-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="5b4bd-110">Na stránce **Vratné certifikáty** v poli **Typ daně** vyberte **TDS**.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="5b4bd-111">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="5b4bd-112">Do pole **Číslo certifikátu** zadejte číslo certifikátu TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="5b4bd-113">V poli **Typ účtu** vyberte typ účtu, pro který je certifikát TDS přijat: **Prodejce**, **Zákazník** nebo **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="5b4bd-114">V poli **Účet** vyberte číslo účtu dodavatele, zákazníka nebo hlavní knihy v závislosti na typu účtu, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="5b4bd-115">Pole **Název** pole zobrazuje název účtu dodavatele, zákazníka nebo hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="5b4bd-116">Do pole **Částka certifikátu** zadejte částku certifikátu TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="5b4bd-117">Do pole **Datum** zadejte datum pro číslo certifikátu.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="5b4bd-118">Vyberte **Dotazy** k otevření stránky **Transakce s certifikáty**, kde můžete zobrazit transakce TDS, pro které je aktualizováno číslo a datum certifikátu TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="5b4bd-119">Tyto informace lze aktualizovat na stránce **Aktualizovat certifikát** stránka (**Daň \> Přiznání \> Srážková daň \> Aktualizovat certifikát**).</span><span class="sxs-lookup"><span data-stu-id="5b4bd-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="5b4bd-120">Stránka **Aktualizovat certifikát** zobrazuje následující informace pro každou transakci TDS:</span><span class="sxs-lookup"><span data-stu-id="5b4bd-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="5b4bd-121">**Datum** – datum zaúčtování transakce TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="5b4bd-122">**Doklad** – Zobrazí pro danou transakci TDS číslo dokladu.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="5b4bd-123">**Zdroj** – Modul, ve kterém byla transakce TDS vytvořena.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="5b4bd-124">**Účet** – Číslo účtu dodavatele, zákazníka nebo hlavní knihy, pro které byla vytvořena transakce TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="5b4bd-125">**Název** – Název účtu dodavatele, zákazníka nebo hlavní knihy, pro které byla vytvořena transakce TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="5b4bd-126">**Částka** – Částka faktury, podle které byla TDS vypočítána.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="5b4bd-127">**Výše daně** – Částka daně TDS, která byla vypočítána pro transakci.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="5b4bd-128">**Datum certifikátu** – Datum certifikátu TDS, které bylo aktualizováno pro transakci TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="5b4bd-129">**Číslo certifikátu** – Číslo certifikátu TDS, které bylo aktualizováno pro transakci TDS.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="5b4bd-130">Na stránce **Vratné certifikáty** vyberte políčko **Zavřeno** k zavření čísla certifikátu TDS po dokončení jeho aktualizace pro transakce TDS na stránce **Aktualizovat certifikát**.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="5b4bd-131">Chcete-li zaškrtnout políčko **Uzavřeno** u všech záznamů na stránce, vyberte **Označit vše**.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5b4bd-132">Čísla certifikátů TDS, která je políčko **Uzavřeno** zaškrtnuté, nejsou k dispozici na stránce **Aktualizovat certifikát**.</span><span class="sxs-lookup"><span data-stu-id="5b4bd-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
