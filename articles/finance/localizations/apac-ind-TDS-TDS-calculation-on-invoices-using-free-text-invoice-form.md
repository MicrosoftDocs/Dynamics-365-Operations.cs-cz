---
title: Výpočet TDS na fakturách ze stránky faktury ve volném textu
description: Toto téma vysvětluje, jak vypočítat daň odečtenou u zdroje (TDS) na fakturách pomocí stránky faktury s volným textem.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023094"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="afa41-103">Výpočet TDS na fakturách ze stránky faktury ve volném textu</span><span class="sxs-lookup"><span data-stu-id="afa41-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afa41-104">Toto téma vysvětluje, jak vypočítat daň odečtenou u zdroje (TDS) na fakturách pomocí stránky **Faktura s volným textem**.</span><span class="sxs-lookup"><span data-stu-id="afa41-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="afa41-105">Přejděte na **Pohledávky \> Faktury \> Všechny volné faktury**.</span><span class="sxs-lookup"><span data-stu-id="afa41-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="afa41-106">[![Stránka Volná faktura](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="afa41-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="afa41-107">Vybráním možnosti **Nové** vytvořte fakturu s volným textem a poté zadejte požadované informace.</span><span class="sxs-lookup"><span data-stu-id="afa41-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="afa41-108">Vyberte kartu **Faktura**. V části **Skupina srážkové daně** pole **Povaha posuzovaného** ukazuje povahu hodnocené kategorie zákazníka.</span><span class="sxs-lookup"><span data-stu-id="afa41-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="afa41-109">V poli **Skupina TDS** zobrazte nebo upravte výchozí skupinu TDS definovanou pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="afa41-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="afa41-110">Když vyberete hodnotu v poli **Skupina TDS**, pole **Skupina TCS** není k dispozici.</span><span class="sxs-lookup"><span data-stu-id="afa41-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="afa41-111">TDS se počítá, pouze pokud je možnost **Vypočítat srážkovou daň** je nastavena na **Ano** pro zákazníka na stránce **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="afa41-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="afa41-112">Na kartě **Daňové údaje** v části **Informace o společnosti** v poli **Název** můžete vybrat název společnosti pro alternativní adresu, která je pro společnost nastavena.</span><span class="sxs-lookup"><span data-stu-id="afa41-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="afa41-113">V části **Srážková daň** pole **Číslo daňového účtu (TAN)** zobrazuje číslo daňového účtu (TAN) pro vybranou společnost.</span><span class="sxs-lookup"><span data-stu-id="afa41-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="afa41-114">Na kartě **Řádky faktury** vytvořte řádky faktury a zadejte požadované údaje.</span><span class="sxs-lookup"><span data-stu-id="afa41-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="afa41-115">V části **Skupina pro srážkovou daň** pole **Číslo daňového účtu (TAN)** ukazuje TAN a pole **Skupina TDS** pole zobrazuje skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="afa41-116">Vyberte **Srážková daň** k otevření stránky **Dočasné transakce srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="afa41-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="afa41-117">Horní část této stránky obsahuje následující pole:</span><span class="sxs-lookup"><span data-stu-id="afa41-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="afa41-118">**Částka srážkové daně celkem** – Celková TDS, která byla vypočítána pro transakci pro skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="afa41-119">**Hodnota** – Celkové procento, které bylo použito k výpočtu TDS pro transakci.</span><span class="sxs-lookup"><span data-stu-id="afa41-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="afa41-120">Celkové procento je založeno na vzorci, který je definován pro daňové kódy TDS a je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="afa41-121">**Upravená částka srážkové daně celkem** – Celková upravená částka TDS pro všechny daňové kódy ve skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="afa41-122">**TDS** – Vybrané zaškrtávací políčko označuje, že je k transakci připojena skupina TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="afa41-123">Políčka na kartách **Přehled**, **Všeobecné** a **Vyrovnání** zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="afa41-124">Vyberte **Mezní hodnota** k otevření stránky **Práh**, kde můžete zkontrolovat mezní limit definovaný pro daňovou složku TDS, která je připojena ke konkrétnímu daňovému kódu TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="afa41-125">Vyberte **Návrhář vzorců** k otevření stránky **Návrhář vzorců**, kde můžete zkontrolovat vzorec definovaný pro konkrétní daňový kód TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="afa41-126">Zaúčtujte fakturu s volným textem.</span><span class="sxs-lookup"><span data-stu-id="afa41-126">Post the free text invoice.</span></span> <span data-ttu-id="afa41-127">Vypočítaná částka TDS, která je vypočítána pro fakturu s volným textem, se zaúčtuje na účet pohledávek, který je definován pro každý daňový zákon TDS ve skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="afa41-128">Účty pohledávek pro daňové kódy TDS jsou definovány na stránce **Kódy srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="afa41-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="afa41-129">Vyberte **Zaúčtovaná srážková daň** k otevření stránky **Transakce srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="afa41-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="afa41-130">Pole **Hodnota** zobrazuje celkové procento, které bylo použito k výpočtu TDS pro transakci.</span><span class="sxs-lookup"><span data-stu-id="afa41-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="afa41-131">Pole na kartách **Přehled**, **Všeobecné** a **Množství** zobrazují částky TDS, které byly vypočítány na řádcích faktury.</span><span class="sxs-lookup"><span data-stu-id="afa41-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="afa41-132">Zkontrolujte informace o výpočtu TDS pro každý daňový kód TDS, který je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="afa41-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
