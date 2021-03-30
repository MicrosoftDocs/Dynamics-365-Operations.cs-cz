---
title: Stornování zaúčtované leasingové transakce
description: Toto téma vysvětluje, jak zrušit zaúčtovanou leasingovou transakci. Jakoukoli transakci vytvořenou prostřednictvím leasingu aktiv lze stornovat.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 22d8eee22221efaf5e7a715c8b95dff261bee62f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249718"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="57440-104">Stornování zaúčtované leasingové transakce</span><span class="sxs-lookup"><span data-stu-id="57440-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57440-105">Jakoukoli transakci vytvořenou prostřednictvím leasingu aktiv lze stornovat.</span><span class="sxs-lookup"><span data-stu-id="57440-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="57440-106">Transakce, které jsou stornovány prostřednictvím leasingu aktiv, aktualizují vaše data leasingu.</span><span class="sxs-lookup"><span data-stu-id="57440-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="57440-107">Proto také aktualizují účetní hodnoty závazku z leasingu a používaný majetek.</span><span class="sxs-lookup"><span data-stu-id="57440-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="57440-108">Chcete-li vytvořit stornovací transakci pro leasing, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="57440-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="57440-109">Na stránce **Majetkové transakce** nebo **Odpovědnost za transakce** vyberte transakci a poté vyberte **Stornovat transakce**.</span><span class="sxs-lookup"><span data-stu-id="57440-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="57440-110">V dialogovém okně, které se zobrazí, můžete upravit datum, kdy bude zaúčtována stornovací položka.</span><span class="sxs-lookup"><span data-stu-id="57440-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="57440-111">Ve výchozím nastavení je pole **Datum** je nastaveno na datum zaúčtování vybrané transakce.</span><span class="sxs-lookup"><span data-stu-id="57440-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="57440-112">Stornující položku nelze zaúčtovat dříve než původní datum zaúčtování vybrané transakce.</span><span class="sxs-lookup"><span data-stu-id="57440-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="57440-113">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="57440-113">Select **OK**.</span></span> <span data-ttu-id="57440-114">Zaúčtuje se položka deníku, která stornuje záznam, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="57440-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="57440-115">Stornování je zobrazeno na stránce **Majetkové transakce** nebo **Transakce závazku** a čistý součet aktuálního zůstatku, který je na stránce zobrazen, se aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="57440-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="57440-116">Když vyberete **Trasování storna**, zobrazí se dialogové okno, které zobrazuje původní transakce i stornované transakce spolu s propojeným číslem, které je známé jako *číslo trasování*.</span><span class="sxs-lookup"><span data-stu-id="57440-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="57440-117">Aby bylo možné storna snáze pochopit a zlepšit viditelnost, můžete je sledovat také pomocí plánů leasingu.</span><span class="sxs-lookup"><span data-stu-id="57440-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="57440-118">Pole **Poslední číslo deníku** na stránce **Plán** zobrazuje čísla deníků transakcí.</span><span class="sxs-lookup"><span data-stu-id="57440-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="57440-119">Když je transakce stornováno, toto pole je aktualizováno číslem deníku stornované transakce.</span><span class="sxs-lookup"><span data-stu-id="57440-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="57440-120">Kromě toho je zaškrtnuto políčko **Stornováno** označující, že transakce byla zrušena, a je vybráno pole **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="57440-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="57440-121">Odvolání stornované transakce</span><span class="sxs-lookup"><span data-stu-id="57440-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="57440-122">Chcete-li odvolat stornovanou transakci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="57440-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="57440-123">Na stránce **Plán** nebo **Transakce** vyberte původní transakci.</span><span class="sxs-lookup"><span data-stu-id="57440-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="57440-124">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="57440-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="57440-125">Pokud jste vybrali transakci na stránce **Plán**, postupujte podle pokynů pro vytvoření deníku v části [Vytvoření měsíčních záznamů deníku v dávce](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="57440-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="57440-126">Deník musíte zaúčtovat ručně.</span><span class="sxs-lookup"><span data-stu-id="57440-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="57440-127">Pokud jste vybrali transakci na stránce **Transakce**, vyberte **Stornovat transakci**.</span><span class="sxs-lookup"><span data-stu-id="57440-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="57440-128">Zobrazí se zpráva s oznámením, že toto odvolání je odvoláním dřívějšího zrušení a že můžete upravit datum zaúčtování tohoto odvolání.</span><span class="sxs-lookup"><span data-stu-id="57440-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="57440-129">Obecná obchodní ověření však ovlivňují data, která lze zadat v poli **Datum**.</span><span class="sxs-lookup"><span data-stu-id="57440-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="57440-130">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="57440-130">Select **OK**.</span></span> <span data-ttu-id="57440-131">Zaúčtuje se položka deníku, která stornuje záznam, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="57440-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="57440-132">Stornování je zobrazeno na stránce **Transakce** a čistý celkový aktuální zůstatek se obnoví na hodnotu před prvním stornováním.</span><span class="sxs-lookup"><span data-stu-id="57440-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="57440-133">Dopad, který mělo zrušení na zůstatky, je proto negován.</span><span class="sxs-lookup"><span data-stu-id="57440-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="57440-134">Když vyberete **Trasování storna**, zobrazí se dialogové okno, které zobrazuje původní transakce i stornované transakce spolu s propojeným číslem trasování.</span><span class="sxs-lookup"><span data-stu-id="57440-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="57440-135">Můžete také trasovat odvolání pomocí příslušné stránky **Plány**.</span><span class="sxs-lookup"><span data-stu-id="57440-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="57440-136">Pole **Storno** je vymazáno, zatímco je vybráno pole **Deník zaúčtován**.</span><span class="sxs-lookup"><span data-stu-id="57440-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="57440-137">Pole **Poslední číslo deníku** je dále aktualizováno číslem deníku transakce odvolání a pole **Číslo deníku** je aktualizováno číslem deníku storna.</span><span class="sxs-lookup"><span data-stu-id="57440-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]