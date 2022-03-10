---
title: Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží
description: Tohle téma popisuje postup, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu.
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e753897d1e21ffebbcbfac48abab4b0549c3553f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565248"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží

[!include [banner](../../includes/banner.md)]

Tohle téma popisuje postup, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu. To obvykle provádí přijímající pracovník.

## <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li projít tímto scénářem pomocí ukázkových záznamů a hodnot uvedených v tomto tématu, musíte používat systém, ve kterém jsou nainstalována standardní ukázková data, a než začnete, musíte vybrat právnickou osobu *USMF*.

Místo toho můžete projít tímto scénářem nahrazením hodnot ze svých vlastních dat za předpokladu, že máte k dispozici následující data:

- Musíte mít potvrzenou nákupní objednávku s otevřeným řádkem nákupní objednávky.
- Položka na řádku musí být na skladě. Nesmí používat varianty produktu a nesmí mít sledovací dimenze.
- Položka musí být přidružena ke skupině dimenzí úložiště, která má povolen proces řízení skladu.
- Sklad, který se používá, musí být povolen pro procesy správy skladu a umístění, které používáte pro příjem, musí být řízeno registrační značkou.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Vytvoření záhlaví deníku pro doručení položky, které používá řízení skladu

Následující scénář ukazuje, jak vytvořit záhlaví deníku pro doručení položky, která používá řízení skladu:

1. Ujistěte se, že váš systém obsahuje potvrzenou nákupní objednávku, která splňuje požadavky uvedené v předchozí části. Tento scénář používá nákupní objednávku pro společnost *USMF*, účet dodavatele *1001*, sklad *51* s řádkem objednávky pro *10 PL* (10 palet) čísla položky *M9200*.
1. Poznamenejte si číslo nákupní objednávky, které ještě použijete.
1. Přejděte na **Řízení zásob \> Položky deníku \> Doručení položky \> Doručení položky**.
1. V podokně akcí zvolte **Nový**.
1. Otevře se dialogové okno **Vytvoření deníku řízení skladu**. V poli **Název** vyberte název deníku.
    - Používáte-li ukázková data *USMF* vyberte hodnotu *WHS*.
    - Pokud používáte svá vlastní data, deník, který vyberete, musí mít parametr **Zkontrolovat výdejní skl. místo** nastaven na *Ne* a **Řízení karantény** na *Ne*.
1. Nastavte **Odkaz** na *Nákupní objednávka*.
1. Nastavte **Číslo účtu** na *1001*.
1. Nastavte **Číslo** na číslo nákupní objednávky, které jste identifikovali pro toto cvičení.

    ![Deník doručení položky.](../media/item-arrival-journal-header.png "Deník doručení položky")

1. Vyberte **OK** k vytvoření záhlaví deníku.
1. V sekci **Řádky deníku** vyberte **Přidat řádek** a zadejte následující údaje:
    - **Číslo položky** – nastavte na *M9200*. **Lokalita**, **Sklad** a **Množství** se nastaví na základě údajů o transakcích zásob pro 10 palet (1000 kusů).
    - **Umístění** – Nastavte na *001*. Toto konkrétní umístění nesleduje registrační značky.

    ![Řádek deníku pro doručení položky.](../media/item-arrival-journal-line.png "Řádek deníku pro doručení položky")

    > [!NOTE]
    > Pole **Datum** určuje datum, kdy bude na skladě registrováno množství této položky.  
    >
    > **ID šarže** bude vyplněno systémem, pokud může být jedinečně identifikováno z uvedených informací. V opačném případě bude nutné jej zadat ručně. Toto je povinné pole, které propojí tuto registraci k řádku konkrétního zdrojového dokumentu.  

1. V podokně Akce klikněte na možnost **Ověřit**. To kontroluje, zda je deník připraven k zaúčtování. Jestliže se ověření nezdaří, které bude nutné před zaúčtováním deníku opravit chyby.  
1. Otevře se dialogové okno **Kontrola deníku**. Vyberte **OK**.
1. Prohlédněte si panel zpráv. Měla by se na něm nacházet zpráva že operace byla dokončena.  
1. V podokně akcí zvolte **Zaúčtovat**.
1. Otevře se dialogové okno **Zaúčtování deníku**. Vyberte **OK**.
1. Prohlédněte si panel zpráv. Měli byste vidět zprávu, že operace byla dokončena.
1. Vyberte **Funkce > Příjem produktu** v podokně akcí, čímž aktualizujete řádek nákupní objednávky a zaúčtujte příjemku produktu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
