---
title: Nastavení číselných řad pro výkazy maloobchodu
description: Tento článek popisuje, jak nakonfigurovat číselné řady, které jsou vyžadovány pro výkazy maloobchodu v Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 917d7b7a905a822ca3b1e074055fe0cd4af5555b
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027179"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Nastavení číselných řad pro výkazy maloobchodu

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nakonfigurovat číselné řady, které jsou vyžadovány pro výkazy maloobchodu v Microsoft Dynamics 365 Commerce.

V Dynamics 365 Commerce se používají dva typy výkazů maloobchodu: 

- **Transakční výkazy** jsou určeny k vytvoření a zaúčtování s vysokou frekvencí. Slouží k zaúčtování všech nefinančních transakcí v prodejně do centrály Dynamics 365 Commerce. 
- **Finanční výkazy** jsou určeny k vytvoření a zaúčtování jednou za pracovní den. Zahrnují pouze uzavřené směny z maloobchodních prodejen, které byly odeslány do centrály Commerce prostřednictvím úlohy P.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Konfigurace číselné řady pro zaúčtování výkazu

Po nastavení maloobchodní prodejny v centrále Commerce musíte nakonfigurovat jedinečnou číselnou řadu, která se bude používat pro vytváření výkazů.

Chcete-li nakonfigurovat číselnou řadu pro zaúčtování výkazů v centrále Commerce, postupujte takto.

1. Přejděte na **Správa organizace \> Číselné řady \> Číselné řady**.
1. Vytvořte nový záznam volbami **Nový \> Číselná řada**.
1. Na záložce s náhledem **Identifikace** v poli **Kód číselné řady** zadejte kód číselné řady.
1. V poli **Název číselné řady** zadejte název.
1. Na záložce s náhledem **Parametry rozsahu** v poli **Rozsah** vyberte **Provozní jednotka**.
1. V poli **Provozní jednotka** vyberte prodejnu, pro kterou bude číselná řada použita.
1. Na záložce s náhledem **Segmenty** definujte segmenty.
1. Na záložce s náhledem **Odkaz** nastavte pole **Oblast** na **Maloobchod**.
1. Nastavte pole **Odkaz** pole na **Číslo výkazu** a poté vyberte **OK**.

    ![Záložky s náhledem Identifikace, Parametry rozsahu, Segmenty a Odkazy na stránce Číselné řady.](media/retail-statements-num-seq-setup-01.png)

1. Na záložce s náhledem **Obecné** v sekci **Přidělení čísla** aktualizujte pole **Nejmenší** a **Největší**, aby odpovídala délce **alfanumerického** segmentu, který jste definovali na záložce s náhledem **Segmenty**.
1. Na záložce s náhledem **Výkon** doporučujeme nastavit možnost **Předběžné přidělení** na **Ano** a pole **Množství čísel** na **25**.

    ![Záložky s náhledem Obecné a Výkon na stránce Číselné řady.](media/retail-statements-num-seq-setup-02.png)

1. V panelu Akce volbou **Uložit** uložte provedené změny a zavřete stránku.
