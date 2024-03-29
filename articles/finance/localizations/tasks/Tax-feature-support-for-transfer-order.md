---
title: Podpora daňových funkcí u převodních příkazů
description: Tento článek vysvětluje novou podporu daňové funkce u převodních příkazů, která využívá službu výpočtu daně.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c55d0891ed37d63f89ee09759965ac443db20dc6
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542237"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Podpora daňových funkcí u převodních příkazů

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje informace o výpočtu daně a integraci účtování v převodních příkazech. Tato funkce umožňuje nastavit výpočet daně a účtování v převodních příkazech pro převody akcií. Podle předpisů Evropské unie (EU) o dani z přidané hodnoty (DPH) se převody akcií považují za intrakomunitární dodávku a intrakomunitární pořízení.

Chcete-li konfigurovat a používat tuto funkci, musíte provést tři hlavní kroky:

1. **Nastavení RCS:** Ve službě Regulatory Configuration Service nastavte daňovou funkci, daňové kódy a použitelnost daňových kódů pro určení daňového kódu v převodních příkazech.
2. **Nastavení Dynamics 365 Finance:** Ve Finance zapněte funkci **Daň v převodním příkazu**, nastavte parametry služby výpočtu daně pro zásoby a nastavte základní parametry daně.
3. **Nastavení zásob:** Nastavte konfiguraci zásob pro transakce převodních příkazů.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Nastavte ve službě RCS daně a transakce převodních příkazů

Podle těchto pokynů nastavíte daň, která je zahrnuta v převodním příkazu. Ve zde zobrazeném příkladu je převodní příkaz směrován z Nizozemska do Belgie.

1. Na stránce **Daňové funkce** na kartě **Verze** vyberte verzi konceptu funkce a poté vyberte možnost **Upravit**.

2. Na stránce **Nastavení daňových funkcí** na kartě **Daňové kódy** vyberte příkaz **Přidat** a vytvořte nové daňové kódy. V tomto příkladu jsou vytvořeny tři daňové kódy: **NL-Exempt**, **BE-RC-21** a **BE-RC+21**.

    - Když je převodní příkaz odeslán ze skladu v Nizozemsku, je použito nizozemský daňový kód osvobození od DPH (**NL-Exempt**) .
      
        Vytvořte daňový kód **NL-Exempt**.
        1. Vyberte příkaz **Přidat** a zapište **NL-Exempt** do pole **Daňový kód**.
        2. Vyberte hodnotu **Podle čisté částky** v poli **Daňová komponenta**.
        3. Zvolte možnost **Uložit**.
        4. Vyberte příkaz **Přidat** v tabulce **Sazba**.
        5. Nastavte pole **Je osvobozeno** na **Ano** v části **Všeobecné**.
        6. Do pole **Kód osvobození** zadejte **EC**.

    - Když je v belgickém skladu přijat převodní příkaz, použije se mechanismus přenesení daňové povinnosti pomocí daňových kódů **BE-RC-21** a **BE-RC+21**.
        
        Vytvořte daňový kód **BE-RC-21**.      
        1. Vyberte příkaz **Přidat** a zapište **BE-RC-21** do pole **Daňový kód**.
        2. Vyberte hodnotu **Podle čisté částky** v poli **Daňová komponenta**.
        3. Zvolte **Uložit**.
        4. Vyberte příkaz **Přidat** v tabulce **Sazba**.
        5. Zapište **-21** do pole **Sazba daně**.
        6. Nastavte pole **Je přenesení daňové povinnosti** na **Ano** v části **Všeobecné**.
        7. Zvolte **Uložit**.
        
        Vytvořte daňový kód **BE-RC+21**.
        1. Vyberte příkaz **Přidat** a zadejte **BE-RC+21** do pole **Daňový kód**.
        2. Vyberte hodnotu **Podle čisté částky** v poli **Daňová komponenta**.
        3. Zvolte **Uložit**.
        4. Vyberte příkaz **Přidat** v tabulce **Sazba**.
        5. Zapište **21** do pole **Sazba daně**.
        6. Zvolte možnost **Uložit**.

3. Definujte daňovou skupinu.
    1. Vyberte **Správa sloupců** a poté vyberte řádkové pole **Daňová skupina**.
    2. Vyberte **->** a pak vyberte **OK**.
    3. Volbou **Přidat** přidejte daňovou skupinu.
    4. Do sloupce **Daňová skupina** zadejte **AR-EU** a poté vyberte daňový kód **NL-Exempt**.
    5. Volbou **Přidat** přidejte daňovou skupinu.
    6. Ve sloupci **Daňová skupina** zadejte **RC-VAT** a poté vyberte daňové kódy **BE-RC-21** a **BE-RC+21**.
4. Definujte daňovou skupinu položky.
    1. Vyberte **Správa sloupců** a poté vyberte řádkové pole **Daňová skupina položky**.
    2. Vyberte **->** a pak vyberte **OK**.
    3. Volbou **Přidat** přidejte daňovou skupinu položky.
    4. Zadejte **FULL** do sloupce **Daňová skupina položky**. Vyberte daňové kódy **BE-RC-21**, **BE-RC+21** a **NL-Exempt**.
5. Definujte použitelnost daňové skupiny.

    1. Vyberte příkaz **Spravovat sloupce** a poté vyberte sloupce, které budou použity k sestavení tabulky použitelnosti.

        > [!NOTE]
        > Nezapomeňte do tabulky přidat sloupce **Obchodní proces** a **Daňové pokyny**. Oba sloupce jsou nezbytné pro funkčnost daně v převodních příkazech.

    2. Přidejte pravidla použitelnosti. Pole **Daňová skupina** nenechávejte prázdné.
        
        Přidejte nové pravidlo pro dodávku převodního příkazu.
        1. Vyberte příkaz **Přidat** v tabulce **Pravidla použitelnosti**.
        2. V poli **Obchodní proces** vyberte **Zásoby**, aby bylo pravidlo použitelné na převodní příkaz.
        3. V poli **Odeslat ze země / oblasti** zadejte **NLD**.
        4. V poli **Odeslat do země / oblasti** zadejte **BEL**.
        5. V poli **Směr daně** vyberte **Výstup**, aby bylo pravidlo použitelné na dodávku převodního příkazu.
        6. V poli **Daňová skupina** vyberte položku **AR-EU**.
        
        Přidejte další pravidlo pro příjemku převodního příkazu.
        
        1. Vyberte příkaz **Přidat** v tabulce **Pravidla použitelnosti**.
        2. V poli **Obchodní proces** vyberte **Zásoby**, aby bylo pravidlo použitelné na převodní příkaz.
        3. V poli **Odeslat ze země / oblasti** zadejte **NLD**.
        4. V poli **Odeslat do země / oblasti** zadejte **BEL**.
        5. V poli **Směr daně** vyberte **Vstup**, aby bylo pravidlo použitelné na příjemku převodního příkazu.
        6. V poli **Daňová skupina** vyberte položku **RC-VAT**.

6. Definujte použitelnost daňové skupiny položky.

    1. Vyberte příkaz **Spravovat sloupce** a poté vyberte sloupce, které budou použity k sestavení tabulky použitelnosti.
    2. Přidejte pravidla použitelnosti.
        
       > [!NOTE]
       > Pokud je výchozí skupina položek daně z obratu na řádcích vašeho zdanitelného dokladu již správná, ponechte tuto matici prázdnou. 
        
        Přidejte nové pravidlo pro dodávku a příjem převodního příkazu.
        1. Na stránce **Pravidla použitelnosti** vyberte **Přidat**.
        2. V poli **Obchodní proces** vyberte **Zásoby**, aby bylo pravidlo použitelné na převodní příkaz.
        3. V poli **Daňová skupina položky** vyberte položku **FULL**.
7. Dokončete a publikujte novou verzi daňové funkce.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Nastavte v aplikaci Finance daně a transakce převodních příkazů

Chcete-li povolit a nastavit daně pro převodní příkazy, postupujte takto:

1. Ve Finance přejděte na **Pracovní prostory** > **Správa funkcí**.
2. V seznamu najděte a vyberte funkci **Daň v převodním příkazu** a poté ji zapněte výběrem možnosti **Povolit**.

    > [!IMPORTANT]
    > Funkce **Daň v převodním příkazu** plně závisí na službě výpočtu daně. Lze ji tedy zapnout až po instalaci služby výpočtu daně.

    ![Daň ve funkci převodního příkazu.](../media/image7.png)

3. Povolte službu výpočtu daně a vyberte obchodní proces **Zásoby**.

    > [!IMPORTANT]
    > Tento krok musíte dokončit pro každou právnickou osobu ve Finance, kde chcete mít k dispozici službu výpočtu daně a funkce daně v převodních příkazech.

    1. Přejděte do nabídky **Daň** > **Nastavení** > **Daňová konfigurace** > **Parametry výpočtu daně**.
    2. V poli **Obchodní proces** vyberte **Zásoby**.

4. Zkontrolujte, zda je nastaven mechanismus přenesení daňové povinnosti. Přejděte do nabídky **Hlavní kniha** \> **Nastavení** \> **Parametry** a poté na kartě **Přenesená daňová povinnost** ověřte, že je možnost **Povolit přenesenou daňovou povinnost** nastavena na **Ano**.

    ![Povolení přenesené daňové povinnosti.](../media/image9.png)

5. Ověřte, že související daňové kódy, daňové skupiny, daňové skupiny zboží a DIČ byly v aplikaci Finance nastaveny podle pokynů služby výpočtu daně.
6. Nastavte účet prozatímního tranzitu. Tento krok je vyžadován pouze v případě, že se daň, která se vztahuje na převodní příkaz, nevztahuje na mechanismus osvobození od daně nebo přenesení daňové povinnosti.

    1. Přejděte na **Daň** > **Nastavení** > **DPH** > **Účetní skupiny**.
    2. V poli **Prozatímní tranzit** vyberte účet hlavní knihy.

       ![Výběr účtu prozatímního tranzitu.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Nastavte základní sklad pro transakce převodních příkazů

Podle těchto pokynů nastavte základní sklad, který umožní transakce převodních příkazů.

1. Vytvořte pro své sklady v různých zemích nebo regionech místa odeslání a příjmu a pro každý web přidejte primární adresu.

    1. Přejděte do nabídky **Warehouse Management** > **Nastavení** > **Sklad** > **Pracoviště**.
    2. Výběrem položky **Nový** vytvoříte pracoviště, které později přiřadíte ke skladu.
    3. Opakujte krok 2 pro všechna ostatní pracoviště, které musíte vytvořit.

    > [!NOTE]
    > Jedno z pracovišť, které vytvoříte, by se mělo jmenovat **Tranzit**. V pozdějších krocích tohoto postupu přiřadíte toto pracoviště k tranzitnímu skladu, aby bylo možné zaúčtovat doklady zásob související s daní v transakcích „odeslání“ a „přijetí“ převodních příkazů. Adresa tranzitního pracoviště není pro výpočet daně relevantní. Proto je nemůžete nechat prázdné.

    ![Nastavení pracovišť.](../media/image11.png)

2. Vytvářejte expediční, tranzitní a dodací sklady. Veškeré informace o adrese uchovávané ve skladu přepíšou adresu pracoviště během výpočtu daně.

    1. Přejděte na **Řízení skladu** > **Nastavení** > **Sklad** > **Sklady**.
    2. Výběrem položky **Nový** vytvoříte sklad a přiřadíte ho k odpovídajícímu pracovišti.
    3. Opakujte krok 2 a podle potřeby vytvořte sklad pro každé pracoviště.

       ![Nastavení skladů.](../media/image12.png)

    > [!NOTE]
    > U expedičního skladu musí být pro transakce převodních příkazů vybrán tranzitní sklad v poli **Tranzitní sklad**.
    >
    > ![Výběr tranzitního skladu.](../media/image13.png)

3. Zkontrolujte, že je pro transakce převodních příkazů nastavena konfigurace zaúčtování zásob.

    1. Přejděte na **Řízení zásob** > **Nastavení** > **Zaúčtování** > **Zaúčtování**.
    2. Na kartě **Zásoby** ověřte, zda je nastaven účet hlavní knihy pro oba typy zaúčtování **Skladový výdej** a **Příjem na sklad**.

        ![Nastavení zaúčtování výdeje a příjmu zásob.](../media/image14.png)

    3. Ověřte, že je nastaven účet hlavní knihy pro zaúčtování **Mezijednotkové závazky**.

        ![Nastavení účtování mezijednotkových závazků.](../media/image15.png)

    4. Ověřte, že je nastaven účet hlavní knihy pro zaúčtování **Mezijednotkové pohledávky**.

        ![Nastavení účtování mezijednotkových pohledávek.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
