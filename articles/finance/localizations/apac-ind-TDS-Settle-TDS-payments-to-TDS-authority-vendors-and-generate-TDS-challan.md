---
title: Vypořádání plateb TDS prodejcům autorit TDS a generování challan TDS
description: Toto téma vysvětluje, jak vyrovnat platby daně odečtené u zdroje (TDS) prodejcům autorit TDS.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023095"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="d1af3-103">Vypořádání plateb TDS prodejcům autorit TDS a generování challan TDS</span><span class="sxs-lookup"><span data-stu-id="d1af3-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1af3-104">Toto téma vysvětluje, jak vyrovnat platby daně odečtené u zdroje (TDS) prodejcům autorit TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="d1af3-105">Přejděte na **Pohledávky \> Platby \> Deník plateb dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="d1af3-106">[![Stránka deníku plateb dodavatelů](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="d1af3-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="d1af3-107">Na stránce **Deník plateb dodavatele** vyberte **Nový** k vytvoření řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="d1af3-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="d1af3-108">V poli **Účet** vyberte dodavatele oprávnění TDS, kterému chcete platby TDS zúčtovat.</span><span class="sxs-lookup"><span data-stu-id="d1af3-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="d1af3-109">Vyberte **Transakce vypořádání** k otevření stránky **Transakce vypořádání**, kde můžete zobrazit vypořádané transakce TDS pro dodavatele oprávnění TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="d1af3-110">Vypořádané transakce TDS za zúčtovací období se zobrazují následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="d1af3-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="d1af3-111">Transakce TDS, kde je povaha kategorie posuzovaného **Společnost**, jsou zobrazeny jako jeden řádek transakce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="d1af3-112">Transakce TDS, kde je povaha kategorie posuzovaného **HUF**, **Firma**, **Osoba**, **AOP**, **BOI**, **Obecní úřad** nebo **Ostatní**, jsou zobrazeny jako jeden řádek transakce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="d1af3-113">Pole **Množství** zobrazuje celkovou částku TDS, která má být zaplacena prodejci autorit TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="d1af3-114">Vyberte **Transakce srážkové daně** k zobrazení různých transakcí TDS, které jsou zahrnuty pro záznam vypořádání.</span><span class="sxs-lookup"><span data-stu-id="d1af3-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="d1af3-115">Na této stránce můžete zobrazit rozdělení každé transakce TDS, která byla zahrnuta do procesu vypořádání pro období vypořádání.</span><span class="sxs-lookup"><span data-stu-id="d1af3-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="d1af3-116">Na kartě **Přehled** vyberte zaškrtávací políčko **Označit** pro transakce TDS k vypořádání s dodavatelem autorit TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="d1af3-117">Karta **Přehled** zobrazuje následující informace pro každou otevřenou transakci TDS:</span><span class="sxs-lookup"><span data-stu-id="d1af3-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="d1af3-118">**Datum** – Datum transakce TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="d1af3-119">**Doklad** – Číslo dokladu.</span><span class="sxs-lookup"><span data-stu-id="d1af3-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="d1af3-120">**Zdroj** – Modul, ve kterém je zaúčtována transakce TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="d1af3-121">**Prodejce/zákazník** – Číslo účtu prodejce nebo zákazníka, od kterého se odečte TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="d1af3-122">**Jméno odpočtené osoby/strany** – Jméno prodejce nebo zákazníka, od kterého se odečte TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="d1af3-123">**Povaha posuzovaného** – Povaha kategorie posuzovaného, do které odpočtená osoba patří.</span><span class="sxs-lookup"><span data-stu-id="d1af3-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="d1af3-124">**Částka** – Částka faktury, podle které byla TDS vypočítána.</span><span class="sxs-lookup"><span data-stu-id="d1af3-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="d1af3-125">**Výše daně** – Částka TDS, která byla vypočítána pro transakci.</span><span class="sxs-lookup"><span data-stu-id="d1af3-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1af3-126">Zrušte zaškrtnutí políčka **Označit** pro všechny transakce TDS, které by neměly být vypořádány prodejci autorit TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="d1af3-127">Na kartě **Všeobecné** je v poli **PAN** zobrazeno trvalé číslo účtu (PAN) příjemce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="d1af3-128">Pole **Datum** zobrazuje datum výpočtu TDS a pole **Hodnota** zobrazuje celkové procento, které bylo použito pro výpočet TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="d1af3-129">Vyberte **Doklad** k zobrazení položek dokladu pro transakci TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="d1af3-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d1af3-130">Close the page.</span></span>
10. <span data-ttu-id="d1af3-131">Vyberte **Složky srážkové daně** k otevření stránky **Složky srážkové daně**, kde si můžete prohlédnout TDS, která byla vypočítána podle daňové složky TDS pro konkrétní daňový kód TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="d1af3-132">Na kartě **Přehled** pole **Daňová složka** zobrazuje TDS daňovou složku, která byla použita pro transakci.</span><span class="sxs-lookup"><span data-stu-id="d1af3-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="d1af3-133">Pole **Částka** pole zobrazuje částku TDS, která byla vypočtena pro daňovou složku TDS, v základní měně.</span><span class="sxs-lookup"><span data-stu-id="d1af3-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="d1af3-134">Pole **Kumulovaná částka** zobrazuje celkovou částku TDS, která byla vypočtena pro daňovou složku TDS pro všechny vypořádané transakce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="d1af3-135">Na kartě **Částka** část **Výchozí měna** ukazuje částku TDS, která byla vypočtena pro daňovou složku TDS, ve výchozí měně.</span><span class="sxs-lookup"><span data-stu-id="d1af3-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="d1af3-136">V části **Sekundární měna** je částka v sekundární měně.</span><span class="sxs-lookup"><span data-stu-id="d1af3-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="d1af3-137">Zavřete stránku **Složky srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="d1af3-138">Na stránce **Otevřené úpravy transakcí** v poli **Množství** si všimněte si, že je aktualizována celková částka k vypořádání dodavateli autority TDS za zúčtovací období.</span><span class="sxs-lookup"><span data-stu-id="d1af3-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="d1af3-139">Chcete-li vypořádat transakce TDS různých období vypořádání TDS prodejci autorit TDS, zaškrtněte políčko **Označit** pro transakce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="d1af3-140">Zavřete stránku **Otevřené úpravy transakcí**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1af3-141">Pokud je pro vypořádání vybráno jen několik transakcí na stránce **Transakce srážkové daně**, celková částka TDS vybraných transakcí se aktualizuje v poli **Oprava** na stránce **Otevřené úpravy transakcí**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="d1af3-142">Částka opravy je aktualizována na řádku deníku na stránce **Doklad deníku** stránka a stránka **Otevřené úpravy transakcí** se zavře.</span><span class="sxs-lookup"><span data-stu-id="d1af3-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="d1af3-143">Na stránce **Doklad deníku** pole **Debet** zobrazuje celkovou částku, která se má zaplatit prodejci autorit TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="d1af3-144">Zadejte údaje offsetového účtu.</span><span class="sxs-lookup"><span data-stu-id="d1af3-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1af3-145">Pokud transakce TDS mají různá čísla daňových účtů (TAN), vytvářejí se řádky deníku za TAN na stránce **Doklad deníku**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="d1af3-146">Na kartě **Poplatek za platbu** v poli **ID poplatku** vyberte ID poplatku, který má typ poplatku **Úrok** nebo **Ostatní** k účtování poplatku za zpoždění plateb provedených prodejci orgánu TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="d1af3-147">Na kartě **Daňové údaje** v části **Informace o společnosti** pole **Název** zobrazuje název společnosti.</span><span class="sxs-lookup"><span data-stu-id="d1af3-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="d1af3-148">V části **Srážková daň** pole **Číslo daňového účtu (TAN)** ukazuje TAN, který je připojen k řádku transakce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="d1af3-149">Proveďte ověření a zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="d1af3-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="d1af3-150">Vyberte **Srážková daň \> Informace challan** pro zadání údajů challan o transakci.</span><span class="sxs-lookup"><span data-stu-id="d1af3-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="d1af3-151">Pole **Doklad** zobrazuje číslo dokladu transakce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="d1af3-152">Zaškrtněte políčko **TDS uloženo zápisem do knihy**, pokud je částka TDS uložena pomocí zápisu do knihy.</span><span class="sxs-lookup"><span data-stu-id="d1af3-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="d1af3-153">Do pole **Číslo challan** zadejte číslo challan, které se používá k provedení platby prodejci orgánu TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="d1af3-154">Do pole **Datum** zadejte datum challan.</span><span class="sxs-lookup"><span data-stu-id="d1af3-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="d1af3-155">V poli **Název banky** vyberte název banky, do které má být vložena částka TDS splatná dodavateli orgánu TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="d1af3-156">Toto pole obsahuje seznam všech bankovních účtů, které byly nastaveny pro dodavatele autorit TDS na adrese **Splatné účty \> Všichni prodejci \> Nastavení \> Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="d1af3-157">Do pole **Kód BSR** pole zadejte kód základní statistické návratnosti (BSR) banky.</span><span class="sxs-lookup"><span data-stu-id="d1af3-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="d1af3-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d1af3-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="d1af3-159">Příklad</span><span class="sxs-lookup"><span data-stu-id="d1af3-159">Example</span></span>

<span data-ttu-id="d1af3-160">Období 04.01.2009 je zúčtováno pro skupinu komponent TDS **Pronájem** pomocí periodického procesu zúčtování TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="d1af3-161">Celková částka TDS 141 625,00 se zaúčtuje na účet autority dodavatele TDS pro období vypořádání TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="d1af3-162">Tuto částku můžete zobrazit v poli **Částka** na stránce **Otevřené úpravy transakcí** pro dodavatele autority TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="d1af3-163">Pokud vyberete **Transakce srážkové daně**, k zobrazení různých transakcí TDS, které byly vypořádány za dané období, se zobrazí následující informace.</span><span class="sxs-lookup"><span data-stu-id="d1af3-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="d1af3-164">Částka TDS</span><span class="sxs-lookup"><span data-stu-id="d1af3-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="d1af3-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-165">16,995.00</span></span>  |
| <span data-ttu-id="d1af3-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-166">22,660.00</span></span>  |
| <span data-ttu-id="d1af3-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-167">28,325.00</span></span>  |
| <span data-ttu-id="d1af3-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-168">16,995.00</span></span>  |
| <span data-ttu-id="d1af3-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-169">28,325.00</span></span>  |
| <span data-ttu-id="d1af3-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-170">16,995.00</span></span>  |
| <span data-ttu-id="d1af3-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-171">11,330.00</span></span>  |

<span data-ttu-id="d1af3-172">Pro konkrétní částku Vyberte **Složky srážkové daně** k zobrazení TDS, která byla vypočítána podle daňové složky TDS pro konkrétní daňový kód TDS.</span><span class="sxs-lookup"><span data-stu-id="d1af3-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="d1af3-173">V tomto příkladu vyberete **Složky srážkové daně** pro částku TDS 16 995,00.</span><span class="sxs-lookup"><span data-stu-id="d1af3-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="d1af3-174">Zobrazí se částka daně, která byla vypočtena pro jednotlivé komponenty transakce.</span><span class="sxs-lookup"><span data-stu-id="d1af3-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="d1af3-175">Daňová komponenta</span><span class="sxs-lookup"><span data-stu-id="d1af3-175">Tax component</span></span> | <span data-ttu-id="d1af3-176">Množství</span><span class="sxs-lookup"><span data-stu-id="d1af3-176">Amount</span></span>    | <span data-ttu-id="d1af3-177">Akumulovaná částka</span><span class="sxs-lookup"><span data-stu-id="d1af3-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="d1af3-178">TDS</span><span class="sxs-lookup"><span data-stu-id="d1af3-178">TDS</span></span>           | <span data-ttu-id="d1af3-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-179">1,5000.00</span></span> | <span data-ttu-id="d1af3-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-180">125,000.00</span></span>         |
| <span data-ttu-id="d1af3-181">Příplatek</span><span class="sxs-lookup"><span data-stu-id="d1af3-181">Surcharge</span></span>     | <span data-ttu-id="d1af3-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-182">1,500.00</span></span>  | <span data-ttu-id="d1af3-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-183">12,500.00</span></span>          |
| <span data-ttu-id="d1af3-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="d1af3-184">PE-Cess</span></span>       | <span data-ttu-id="d1af3-185">330.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-185">330.00</span></span>    | <span data-ttu-id="d1af3-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-186">2,750.00</span></span>           |
| <span data-ttu-id="d1af3-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="d1af3-187">SHE Cess</span></span>      | <span data-ttu-id="d1af3-188">165.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-188">165.00</span></span>    | <span data-ttu-id="d1af3-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="d1af3-189">1,375.00</span></span>           |

<span data-ttu-id="d1af3-190">Pokud jste vybrali pouze částky TDS 16 995,00, 22 660,00 a 28 325,00 pro vypořádání na stránce **Transakce srážkové daně**, celková částka pro vypořádání se zobrazuje jako **67 980,00** v poli **Oprava** na stránce **Otevřené úpravy transakcí**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="d1af3-191">Pokud je tato transakce označena k vypořádání a stránka **Otevřené úpravy transakcí** je zavřená, částka **67 980,00** je zobrazen v poli **Debet** na stránce **Doklad deníku**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="d1af3-192">Nyní můžete zaúčtovat deník a vygenerovat TDS challan.</span><span class="sxs-lookup"><span data-stu-id="d1af3-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="d1af3-193">Úprava zálohových plateb, které jsou prováděny prodejcům autorit TDS</span><span class="sxs-lookup"><span data-stu-id="d1af3-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="d1af3-194">Chcete-li upravit zálohu, která byla provedena prodejci orgánu TDS, na skutečnou platbu, přejděte na **Závazky \> Prodejci \> Všichni prodejci \> Úpravy transakcí**.</span><span class="sxs-lookup"><span data-stu-id="d1af3-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="d1af3-195">Pokud skutečná platba, která je provedena, přesahuje zálohu, jsou pro transakci vygenerována dvě challan čísla.</span><span class="sxs-lookup"><span data-stu-id="d1af3-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="d1af3-196">V dotazu TDS se však zobrazuje pouze první číslo challan.</span><span class="sxs-lookup"><span data-stu-id="d1af3-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
