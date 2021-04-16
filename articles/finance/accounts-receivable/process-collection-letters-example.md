---
title: Příklad zpracování upomínek
description: Toto téma prochází příkladem, který ukazuje proces vytváření, tisku a odesílání upomínek.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826340"
---
# <a name="process-collection-letters-example"></a>Příklad zpracování upomínek

[!include [banner](../../includes/banner.md)]

Toto téma prochází příkladem, který ukazuje proces vytváření, tisku a odesílání upomínek. Příklad je založen na možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** v Kredit a výběr. Využívá data demo společnosti USMF a nového zákazníka US-045.

Chcete-li začít, přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci**, vyberte **Nový** a poté zadejte požadované informace k vytvoření zákazníka US-045.

Po dokončení postupujte následovně.

1. Přejděte do **Kredit a výběr \> Upomínka \> Nastavit sekvenci upomínky** a nastavte sekvenci upomínky, jak je znázorněno v následující tabulce, která je přiřazena k profilu odesílání zákazníků.

|     Kód upomínky      |     popis                           |     Měna      |     Hlavní účet        |     Poplatek v měně     |     Minimum přes        |     Blok dní      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Upomínka 1         |     Druhé oznámení s poplatkem        |     USD           |                           |     0,00                  |     0,00                  |     2                 |
|     Upomínka 2         |     Druhé oznámení s poplatkem        |     USC           |     403150                |     20.00                 |     10.00                 |     3                 |
|     Kolekce                    |     Poslední oznámení s poplatkem         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

Následující obrázek ukazuje informace, které jsou v tabulce tak, jak by vypadaly na stránce **Upomínky**. 

[![Nastavení pořadí upomínek](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Nyní musíte nastavit dva parametry požadované pro tento příklad.

2. Přejděte na **Kredit a inkasa \> Nastavení \> Parametry závazků** a postupujte následovně:

    1. Na kartě **Inkasa** nastavte možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** na **Ano**.
    2. Ujistěte se, že pole **Vytvořit upomínku pro** je nastaveno na **Zákazník**.

    [![Nastavení parametrů pohledávek pro inkasa](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Přejděte do **Pohledávky \> Faktury \> Všechny faktury s volným textem**, vyberte **Nový** a potom postupujte podle těchto kroků:

    1. V poli **Účet odběratele** vyberte **US-045**.
    2. Do pole **Datum faktury** zadejte **15. 1. 2021**.
    3. V poli **Splatnost** zadejte hodnotu **16. 1. 2021**.
    4. Na kartě s náhledem **Řádky faktur** v poli **Hlavní účet** zadejte **401100**.
    5. Do pole **Jednotková cena** zadejte **500.00**.
    6. Zvolte **Zaúčtovat**.

    Nyní musíte zadat dva dobropisy pro zákazníka.

4. Vyberte **Nový** a postupujte podle následujících kroků:

    1. V poli **Účet odběratele** vyberte **US-045**.
    2. Do pole **Datum faktury** zadejte **15. 1. 2021**.
    3. V poli **Splatnost** zadejte hodnotu **16. 1. 2021**.
    4. Na kartě s náhledem **Řádky faktur** v poli **Hlavní účet** zadejte **401100**.
    5. Zadejte do pole **Jednotková cena** **−100,00**.
    6. Zvolte **Zaúčtovat**.

5. Opakujte krok 4, ale zadejte **−200,00** do pole **Jednotková cena**.
6. Přejděte na **Pohledávky \> Zákazníci \> Všichni zákazníci** a vyberte zákazníka **US-045**. Poté v podokně akcí vyberte **Transakce \> Transakce** a zkontrolujte zákaznické transakce, které jste zaúčtovali dříve.

    [![Kontrola zaúčtovaných transakcí se zákazníkem](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Nyní musíte vytvořit upomínky pro zákazníka US-045.

7. Přejděte na **Kredit a inkasa \> Upomínka \> Vytvořit upomínky** a postupujte následovně:

    1. Nastavte možnosti **Faktura** a **Dobropis** na **Ano**.

        Ve výchozím nastavení je pole **Upomínka** nastaveno na **Inkaso na zákazníka**.

    2. Do pole **Datum upomínky** zadejte **19. 1. 2021**.
    3. Na kartě s náhledem **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v poli **Zákaznický účet** přidejte zákazníka **US-045**.
    4. Vyberte **OK**.
    5. Výběrem **OK** vytvoříte upomínky.

8. Přejděte na **Kredit a inkasa \> Upomínka \> Zkontrolovat a zpracovat upomínky** a postupujte následovně:

    1. Všimněte si, že kód upomínky na řádcích záhlaví i transakce je **Upomínka 1**, protože tato upomínka je prvním sběrným dopisem v pořadí. (Chcete-li zobrazit řádky transakcí, možná budete muset vybrat kartu s náhledem **Transakce**.)

   [![Ověření, že se v záhlaví a řádcích objeví stejný kód upomínky](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. V podokně akcí zvolte **Zaúčtovat**.
    3. Do pole **Datum zaúčtování** zadejte **19. 1. 2021**.

    Nyní musíte opět vytvořit upomínky pro zákazníka US-045.

9. Přejděte na **Kredit a inkasa \> Upomínka \> Vytvořit upomínky** a postupujte následovně:

    1. Nastavte možnosti **Faktura** a **Dobropis** na **Ano**.

        Ve výchozím nastavení je pole **Upomínka** nastaveno na **Inkaso na zákazníka**.

    2. Do pole **Datum upomínky** zadejte **23. 1. 2021**.
    3. Na kartě s náhledem **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v poli **Zákaznický účet** přidejte zákazníka **US-045**.
    4. Vyberte **OK**.
    5. Výběrem **OK** vytvoříte upomínky.

10. Přejděte na **Kredit a inkasa \> Upomínka \> Zkontrolovat a zpracovat upomínky** a postupujte následovně:

    1. Všimněte si, že kód upomínky v záhlaví je **Upomínka 1**. Kód na řádcích transakce však je **Upomínka 2**.

   [![Ověřuje, že se v záhlaví a řádcích objeví různé kódy upomínky](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Kódy se liší, protože možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** je na **Ano**.

  2. Nezaúčtovat tuto upomínku.

11. Přejděte na **Úvěr a inkasa \> Nastavit \> Parametry pohledávek** a poté na kartě **Inkasa** nastavte **Při výpočtu kódu upomínky ignorovat platby a dobropisy** na **Ne**.

    [![Nastavení možnosti Ignorovat platby a dobropisy pro výpočet kódu upomínky na Ne](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Nyní musíte opět vytvořit upomínky pro zákazníka US-045.

12. Přejděte na **Kredit a inkasa \> Upomínka \> Vytvořit upomínky** a postupujte následovně:

    1. Nastavte možnosti **Faktura** a **Dobropis** na **Ano**.

        Ve výchozím nastavení je pole **Upomínka** nastaveno na **Inkaso na zákazníka**.

    2. Do pole **Datum upomínky** zadejte **23. 1. 2021**.
    3. Na kartě s náhledem **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v poli **Zákaznický účet** přidejte zákazníka **US-045**.
    4. Vyberte **OK**.
    5. Výběrem **OK** vytvoříte upomínky.

13. Přejděte na **Kredit a inkasa \> Upomínka \> Zkontrolovat a zpracovat upomínky** a všimněte si, že kód upomínky na řádcích záhlaví i transakce je **Upomínka 2**.

    [![Další zobrazení, že se v záhlaví a řádcích objeví stejný kód upomínky](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Stejný kód se zobrazuje na obou místech, protože možnost **Při výpočtu kódu upomínky ignorovat platby a dobropisy** je nyní nastavena na **Ne**.
