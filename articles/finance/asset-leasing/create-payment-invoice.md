---
title: Vytvoření platebních faktur
description: Toto téma vysvětluje, jak vytvořit měsíční leasingové faktury. Můžete vytvářet faktury pro jednotlivé leasingy nebo můžete použít dávkové zpracování pro vytvoření více leasingů.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 51e4c44cf192754a832132ea1942baf18b43a755
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815997"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="7ae1b-104">Vytvoření platebních faktur</span><span class="sxs-lookup"><span data-stu-id="7ae1b-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ae1b-105">Můžete vytvářet měsíční faktury pro jednotlivé leasingy nebo můžete použít dávkové zpracování pro vytvoření více leasingů.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="7ae1b-106">Následující postup ukazuje, jak vytvořit samostatnou položku leasingové splátky, když he zapnutý parametr **Platba dodavateli** na stránce **Nastavení leasingové knihy**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="7ae1b-107">Na stránce **Shrnutí leasingu** vyberte leasing a poté vyberte **Knihy \> Platební kalendář**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="7ae1b-108">Vyberte platbu, kterou je třeba provést, a poté vyberte **Vytvořit deník**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="7ae1b-109">Zobrazí se zpráva s oznámením, že k vybrané platbě byl vytvořen deník.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="7ae1b-110">Vyberte **Fakturační deníky** a poté vyberte fakturu, kterou je třeba uhradit.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="7ae1b-111">Na kartě **Řádky** zkontrolujte položku deníku, než ji zaúčtujete do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ae1b-112">Ve výchozím nastavení řádky faktury dodavatele, které jsou vytvořeny, používají profil účtování dodavatele ze stránky **Parametry závazků**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="7ae1b-113">Vyberte správný deník a poté vyberte fakturu, kterou je třeba uhradit.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="7ae1b-114">V tomto příkladu je zapnutý parametr **Platba dodavateli** v leasingové knize.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="7ae1b-115">Faktura proto bude v deníku faktur.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="7ae1b-116">Sekce **Přehled** zobrazuje souhrn položky deníku a sekce **Řádky** obsahuje podrobnosti o samotných řádcích deníku.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ae1b-117">Pokud je parametr **Platba dodavateli** vypnutý, budou položky deníku plateb uvedeny na stránce **Leasing majetku** pro leasingovou knihu a systém vytvoří položku leasingu majetku namísto faktury.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="7ae1b-118">Položka leasingové splátky bude zaúčtována do názvu deníku, který je zadán v poli **Deník měsíčního leasingu**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="7ae1b-119">Po zaúčtování transakce můžete zobrazit informace o transakci a účetní hodnotu leasingového závazku výběrem **Transakce závazku** v leasingové knize.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="7ae1b-120">V platebním kalendáři bude vybráno políčko **Deník zaúčtován** a na řádku bude uvedeno číslo deníku faktury.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="7ae1b-121">Po vytvoření deníku plateb a položky pro tento deník musíte záznam stornovat, než jej lze znovu vytvořit.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]