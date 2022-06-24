---
title: Nastavení a zpracování překlenovacích plateb
description: Tento článek vysvětluje, jak nastavit a zpracovat překlenovací platby zákazníků. Překlenovací platba je platba, která se zaúčtuje do hlavní knihy ve dvou krocích.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f0609e333fb16ba189b6a971f88fbb5bf900fec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887970"
---
# <a name="set-up-and-process-bridged-payments"></a>Nastavení a zpracování překlenovacích plateb

[!include [banner](../includes/banner.md)]

Překlenovací platba je platba, která se zaúčtuje do hlavní knihy ve dvou krocích. Obvykle se tento přístup používá, když je nastaven způsob platby **Banka** a transakce musíte zaúčtovat na bankovní účet až poté, co byla transakce zúčtována bankou. Můžete jej však použít i pro účet hlavní knihy. V tomto případě systém při zpracování překlenovacího zaúčtování přesune částku z jednoho hlavního účtu na jiný hlavní účet.

Překlenovací platby můžete vytvořit ze závazků nebo pohledávek. Ačkoli tento článek vysvětluje, jak nakonfigurovat překlenovací účtování pro pohledávky, kroky pro transakce závazků jsou podobné.

## <a name="set-up-bridging-posting"></a>Nastavení překlenovacího účtování

Chcete-li použít překlenovací účtování, musíte nastavit jeden nebo více způsobů platby tak, aby používal metodu **Překlenovací účtování**. Poté musíte vybrat překlenovací účet.

1. Přejděte do nabídky **Pohledávky &gt; Nastavení platby &gt; Metody platby**.
2. Chcete-li povolit překlenovací účtování, vyberte existující způsob platby. Případně vytvořte nový způsob platby.
3. Zaškrtněte políčko **Překlenovací zaúčtování**.
4. V poli **Překlenovací účet** vyberte hlavní účet, na který mají být platby zaúčtovány před jejich zúčtováním na bankovní účet.
5. Zavřete stránku.

## <a name="process-and-transfer-bridging-posting"></a>Zpracování a převod překlenovacího účtování

Chcete-li vytvořit a zpracovat překlenovací účtování, postupujte následovně.

1. Přejděte na **Pohledávky &gt; Platby &gt; Deník plateb zákazníkovi**.
2. Zvolte **Nový** pro vytvoření deníku.
3. V poli **Název** vyberte název.
4. Přidejte řádky do deníku plateb zákazníka a vyberte způsob platby, který je nakonfigurován pro překlenovací účtování.
5. Zaúčtovat deník Transakce budou zaúčtovány na hlavní účet, který jste vybrali v poli **Překlenovací účet** v předchozím postupu.

Když jsou transakce zúčtovány bankou a chcete převést platbu z překlenovacího účtu na platební účet, který je uveden pro způsob platby, postupujte takto.

1. Přejděte na **Hlavní kniha &gt; Položky deníku &gt; Hlavní deníky**.
2. Zvolte **Nový** pro vytvoření deníku.
3. V poli **Název** vyberte název.
4. Vyberte **Řádky** k otevření údajů deníku.
5. Vyberte **Funkce &gt; Vybrat překlenovací transakce**.
6. Označte každou platbu, která byla zúčtována, a poté vyberte **Přijmout**.
7. Zaúčtovat deník
