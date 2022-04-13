---
title: Zálohy zákazníků
description: Toto téma vysvětluje, jak nastavit a zpracovat zálohy zákazníků (známé také jako vklady zákazníků).
author: twheeloc
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ba462dc2b5fe326db14dfb3c92f986478d31791
ms.sourcegitcommit: 3cb1f49a02e4a849fc34ffeb81fe507f0608b35e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/22/2022
ms.locfileid: "8464869"
---
# <a name="customer-prepayments"></a>Zálohy zákazníků

[!include [banner](../includes/banner.md)]

Zálohy zákazníka se používají, když obdržíte platbu od zákazníka, ale neexistuje žádná faktura, proti které lze platbu uhradit. Tyto typy plateb se také označují jako vklady zákazníků.

Proces nastavení a práce se zálohami zákazníkům se skládá z následujících základních kroků.

1. Vytvořte účetní profil zákazníka pro platby záloh.
2. Nastavte parametr **Účetní profil se zálohovým dokladem deníku**.
3. Vytvořte deník plateb od zákazníka a zaškrtněte políčko **Zálohový doklad deníku** na každém řádku.
4. Zaúčtovat deník plateb odběratele
5. Po vygenerování faktury vyrovnejte zálohovou platbu pomocí stránky **Vypořádat otevřené transakce**.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Vytvoření účetního profilu zákazníka pro platby záloh

Obvykle, když přijmete zálohy nebo vklady od svých zákazníků před dodáním zboží nebo služeb nebo předtím, než ve vašem systému bude existovat faktura, budete chtít zaznamenat hotovost jako závazek namísto majetku v účtové osnově. Požadavky na zaznamenávání těchto částek do hlavní knihy se však mohou lišit v závislosti na vaší zemi nebo oblasti. Nezapomeňte se proto poradit se svými účetními ohledně veškerých platných místních předpisů.

Obecně platí, že proces vytváření profilu účtování, který lze použít pro platby předem, je stejný jako proces vytváření dalších profilů účtování. Primárním rozdílem je hlavní účet, který vyberete v poli **Souhrnný účet**. Další informace naleznete v tématu [Účetní profily zákazníka](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Definování parametrů záloh pro zákazníka

Existují dva hlavní parametry závazků, které musíte vzít v úvahu při konfiguraci systému pro platby záloh zákazníkovi. Při konfiguraci parametrů postupujte následovně.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
2. Volitelné: Na kartě **Hlavní kniha a DPH** na pevné záložce **Platba** nastavte možnost **Daň z prodeje u zálohového dokladu deníku** na **Ano**.
3. V poli **Profil zaúčtování s poukazem na zálohový doklad deníku** vyberte profil účtování zákazníka, který se má použít při zaúčtování záloh zákazníků.
4. Zavřete stránku.

## <a name="create-customer-prepayment-vouchers"></a>Vytvoření zálohových poukazů zákazníka

Při vytváření deníku plateb pro zákazníka musíte pro každou platbu předem nastavit možnost **Zálohový doklad deníku** na **Ano** na stránce **Deník plateb zákazníka**. Pokud chcete zálohu zákazníka, postupujte takto.

1. Přejděte na **Pohledávky \> Platby \> Deník plateb zákazníkovi**.
2. Zvolte **Nový** pro vytvoření deníku.
3. V poli **Název** vyberte název deníku, který chcete použít.

    > [!IMPORTANT]
    > Pokud jste v předchozím postupu nastavili **Daň z obratu na zálohovém dokladu deníku** na **Ano**, musíte vybrat název deníku, kde he vybrán parametr **Částka zahrnuje daň z obratu**. 

4. Volitelné: Do pole **Popis** zadejte podrobný popis.
5. Vybrat **řádky**.
6. Pokud prázdný řádek neexistuje, vyberte **Nový** pro vytvoření řádku.
7. Do pole **Datum** zadejte datum, kdy má být záloha zaúčtována.
8. V poli **Účet** vyberte zákazníka pro zálohu.
9. Volitelné: Do pole **Popis** zadejte podrobný popis transakce.
10. V poli **Kredit** zadejte částku zálohy.
11. V poli **Typ účtu pro protiúčet** vyberte účet pro vyrovnání platby. Vyberte například banku nebo hlavní účet, na který chcete platbu zaúčtovat.
12. V poli **Metoda platby** vyberte metodu platby zákazníka.
13. Na kartě **Způsob platby** nastavte možnost **zálohový doklad deníku** na **Ano**.
14. Opakujte kroky 7 až 13 pro každou další platbu předem, která musí být zaúčtována.
15. Vyberte **Zaúčtovat** pro dokončení deníku.

## <a name="settle-prepayments-with-invoices"></a>Vyrovnání záloh s fakturami

V pracovním prostoru **Platby zákazníkům** můžete snadno vyhledávat a vypořádávat platby, které nebyly zcela vypořádány.

1. V řídicím panelu **Domů** vyberte dlaždici **Platby zákazníka**.
2. V sekci **Zákaznické transakce** na kartě **Platby nejsou vypořádány** vyhledejte a vyberte platbu k vypořádání.
3. Vyberte **Vyrovnat transakce**.
4. Zaškrtněte políčko **Označit** pro fakturu a platbu, která bude vypořádána.
5. Zvolte **Zaúčtovat**.

Další informace o tom, jak vypořádat otevřené transakce, najdete v části [Přehled vyrovnání](/dynamics365/finance/cash-bank-management/settlement-overview).
