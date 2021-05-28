---
title: Chyba, když je zaúčtován Deník dokončené výroby
description: Když zaúčtujete sestavu jako dokončený deník, zobrazí se chybová zpráva s oznámením, že objednané množství nelze snížit.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026326"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="da92e-103">Chyba, když je zaúčtován Deník dokončené výroby</span><span class="sxs-lookup"><span data-stu-id="da92e-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="da92e-104">Číslo článku znalostní báze: 4612891</span><span class="sxs-lookup"><span data-stu-id="da92e-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="da92e-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="da92e-105">Symptoms</span></span>

<span data-ttu-id="da92e-106">Když zaúčtujete deník **Nahlásit jako dokončené**, dojde k chybě a zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="da92e-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="da92e-107">Objednané množství nemůže být sníženo, protože není dostatek otevřených skladových transakcí se stavem Objednáno.</span><span class="sxs-lookup"><span data-stu-id="da92e-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="da92e-108">Položky jsou zakoupené, přijaté nebo registrované.</span><span class="sxs-lookup"><span data-stu-id="da92e-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="da92e-109">K této chybě dochází pouze v případě, že je pole **Chybné množství** nastaveno na prvním řádku deníku **Nahlásit jako dokončené** a pole **Dobré množství** je nastaveno na posledním řádku.</span><span class="sxs-lookup"><span data-stu-id="da92e-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="da92e-110">Pokud je pole **Chybné množství** je nastaveno na posledním řádku, nedojde k žádné chybě.</span><span class="sxs-lookup"><span data-stu-id="da92e-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="da92e-111">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="da92e-111">Resolution</span></span>

<span data-ttu-id="da92e-112">Chcete-li této chybě zabránit, otevřete stránku **Parametry řízení výroby** a poté na kartě **Obecné** nastavte možnost **Zvýšení zůstatku s chybovým množstvím** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="da92e-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
