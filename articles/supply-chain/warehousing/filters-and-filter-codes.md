---
title: Konfigurace produktových filtrů pro skladové transakce
description: Toto téma popisuje, jak konfigurovat filtry pro produkty a kódy filtrů ke kategorizaci skladových položek ve skladu. Filtry lze také použít k určení, kteří odběratelé mohou objednat určité zboží a určit zboží, které lze zakoupit od určitého dodavatele.
author: Mirzaab
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 8c5574efeb1dee372a8ecf8ddb1d1710f63b73a7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345227"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Konfigurace produktových filtrů pro skladové transakce

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak konfigurovat filtry pro produkty a kódy filtrů ke kategorizaci skladových položek ve skladu. Filtry lze také použít k určení, kteří odběratelé mohou objednat určité zboží a určit zboží, které lze zakoupit od určitého dodavatele.

Dále můžete nastavit a používat kódy produktů k automatickému uspořádání skladových položek ve skladu a kombinování filtrovaných položek do skupin filtrů. Filtry lze použít k zařazení položek do kategorií pro procesy manipulace, nákupu a prodeje. Možná budete chtít položky seskupit nebo je od sebe oddělit, pokud způsob manipulace s nimi závisí na hmotnosti nebo omezeních manipulace. Můžete také určit, od kterých zákazníků nebo prodejců lze položku zakoupit nebo prodat.

## <a name="prerequisites"></a>Předpoklady

Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.

| Předpoklad | Pokyny |
|---|---|
| Než začnete konfigurovat produkty na stránce **Podrobnosti o uvolněném produktu**, musíte zapnout zpracování skladu pro skupinu dimenzí úložiště produktu. | Jděte na **Správa informací o produkt \> Nastavení \> Skupiny dimenzí a variant \> Skupiny dimenzí úložiště** a vyberte nebo vytvořte skupinu dimenzí úložiště, kde je možnost **Použít procesy řízení skladu** nastavena na *Ano*. |
| Pokud budete používat zákaznické filtry nebo filtry dodavatelů, musíte povolit jejich použití v parametrech řízení skladu. | Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**. Na kartě **Filtry produktu** nastavte **Povolit zákaznické filtry** a/nebo **Povolit filtry dodavatele** na *Ano*. |

## <a name="set-up-product-filters"></a>Nastavení filtrů produktu

Filtry produktu poskytují až 10 vlastností **Název filtru**, což jsou hodnoty výčtu. Tyto hodnoty výčtu jsou k dispozici pro výběr při vytváření filtru produktu. Hodnoty výčtu *Code 1* až *Code 10* jsou definované systémem a představují konkrétní vlastnost nebo atribut položky. Například *Kód 1* může představovat položky, které mají klasifikaci nebezpečných materiálů. *Kód 2* může představovat položky, které si mohou koupit pouze prodejci. Filtry produktu pak definují konkrétní hodnotu **Kód filtru** spojenou s hodnotou **Název filtru**.

1. Jděte na **Řízení skladu \> Nastavení \> Filtry produktu \> Filtry produktu**.
1. V podokně Akce vyberte možnost **Nový** pro přidání filtru produktu do mřížky.
1. V poli **Název filtru** vyberte hodnotu.
1. Zadejte hodnotu do pole **Kód filtru**.

    ![Nastavení filtru produktu.](media/Product_Filters10.png "Nastavení filtru produktu")

1. Do pole **Popis** zadejte název kódu. Například *Kód 2* může představovat dodavatele. Poté můžete vytvořit produktový filtr pro konkrétního dodavatele nebo skupinu dodavatelů. Více informací naleznete v části [Nastavení kódů filtru dodavatele](#vendor-product-filters) dále v tomto tématu.

    ![Nastavení filtrů produktu.](media/Product_Filters.png "Nastavení filtrů produktu")

## <a name="set-up-product-filter-groups"></a>Nastavení skupin filtru produktu

K seskupení kódů filtru můžete použít skupiny filtrů. Tato schopnost je užitečná, když se skupina používá v dotazu ve směrnici skladového místa, a vy chcete vyhledat skupiny, nikoli série kódů. Každá skupina filtrů je přidružena ke skupině položek.

> [!IMPORTANT]
> Ne všechny skupiny filtrů produktů jsou k dispozici pro kódy filtrů, které jsou vyšší než *Kód 4* (to znamená, *Kód 5* přes *Kód 10*). Například u vydaných produktů se sice přidají všechny kódy filtrů produktů, ale seskupení kódů filtrů se neaktualizuje. Toto chování může být aktualizováno v pozdějších verzích.

Chcete-li nastavit skupiny filtrů, postupujte následujícím způsobem.

1. Jděte na **Řízení skladu \> Nastavení \> Filtry produktu \> Skupiny filtrů produktu**.
1. V podokně akcí zvolte **Nový**.
1. V poli **Skupina 1** a **Skupina 2** zadejte názvy, které budou použity ke kategorizaci položek.
1. Na záložce s náhledem **Detaily** vytvořte nový řádek stisknutím tlačítka **Nový**.
1. V poli **Počáteční datum / čas** a **Koncové datum / čas** zadejte počáteční a koncové datum pro skupinu filtrů.
1. V poli **Skupina položek** vyberte skupinu položek, na kterou by se měl filtr produktu vztahovat.
1. V poli **Kód 1** až **Kód 10** podle potřeby vyberte kódy filtrů, které chcete do skupiny zahrnout.

    ![Sk. položek.](media/ProdFilterGroup.png "Sk. položek")

> [!NOTE]
> Pokud se při zavření stránky zobrazí chybová zpráva, může chybět nastavení kódu. Na stránce **Skupiny položek** můžete označit kódy jako povinné pro skupinu položek zaškrtnutím políček **Přiřadit kód 1 filtru pro skupinu položek**, **Přiřadit kód 2 filtru pro skupinu položek** atd.

## <a name="set-up-filter-codes-on-item-groups"></a>Nastavení kódů filtrů ve skupinách zboží

Nastavením kódů filtrů pro skupinu zboží můžete vyžadovat kódy, které jsou požadované pro produkty připojené k této skupině zboží.

Chcete-li nastavit kódy filtrů pro skupiny zboží postupujte takto.

1. Jděte na **Řízení zásob \> Nastavení \> Sklady \> Skupiny položek**.
1. V podokně Akce vyberte možnost **Nová** a vytvořte novou skupinu položek.
1. V poli **Skupina položek** zadejte název.
1. Do pole **Název** zadejte popis.
1. Na záložce s náhledem **Sklad** v části **Požadovaný filtr** zaškrtněte příslušná políčka k definování jednoho nebo více kódů filtrů, které musí být určeny pro produkty, které jsou přidružené ke skupině zboží.

    Chcete-li aktualizovat vydaný produkt, otevřete jeho stránku **Podrobnosti o vydaném produktu** a poté v podokně akcí vyberte **Upravit**. Filtry, které jsou přidruženy ke kódům, budou poté k dispozici na záložce s náhledem **Sklad**.

    ![Sk. položek.](media/ItemGroup10.png "Sk. položek")

1. V části **Filtr skupin položek** zaškrtněte políčka u filtrů, které se musí shodovat, aby skupina filtrů byla výchozí skupinou filtrů pro položku.

    Například pokud jsou zaškrtnutá políčka **Použít kód 1 filtru** a **Použít kód filtru 2**, kód filtru 1 i 2 pro zboží se bude muset shodovat s nastavením skupiny filtrů pro vybranou skupinu položek před tím, než bude možné vybrat skupinu filtrů. Když vytvoříte novou položku, vybraná skupina filtrů bude výchozí skupinou filtrů **Skupina 1** a **Skupina 2** na záložce s náhledem **Sklad** podokna **Podrobnosti o vydaném produktu**.

> [!IMPORTANT]
> Kódy filtrů produktů jsou povoleny pouze pro položky, které používají pokročilou správu skladu.

## <a name="specify-filter-codes-for-released-products"></a>Zadání kódů filtrů pro uvolněné produkty

Tento postup slouží k zadání kódů filtrů pro uvolněné produkty. Například můžete použít kódy filtrů ke seskupení nebezpečných produktů, které kupují konkrétní prodejci.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. V podokně akcí vyberte možnost **Nový** a vytvořte produkt.
1. V dialogovém okně **Nově vydaný produkt** zadejte data, která jsou nutná k vytvoření základny nového produktu, a poté vyberte **OK**.

    Kódy filtrů produktů nejsou povoleny, pokud skupina položek připojená k produktu nebyla nakonfigurována pro kódy filtrů.

    Další informace naleznete v tématu [Vytvoření nového produktu](../pim/tasks/create-new-product.md).

1. Na kartě s náhledem **Sklad** v části **Kódy filtru produktu** vyberte kódy filtrů pro pole **Kód 1** až **Kód 10**, jak je požadováno k určení kódů filtru pro produkt.

## <a name="set-up-generally-available-items"></a>Nastavení obecně dostupných položek

Můžete zpřístupnit konkrétny skladové položky pouze pro odběratele, dodavatele nebo pro odběratele i dodavatele.

> [!NOTE]
> Na všechny položky, které nastavíte jako obecně dostupné, se nevztahují filtry odběratelů ani filtry dodavatelů.

Chcete-li nastavit obecně dostupné položky postupujte podle následujících kroků.

1. Jděte na **Řízení skladu \> Nastavení \> Filtry produktu \> Obecně dostupné produkty**.
1. V podokně akcí vyberte možnost **Nový** a vytvořte záznam.
1. V poli **Odběratel nebo dodavatel** vyberte *Odběratel*, *Dodavatel* nebo *Vše* ke zpřístupnění položek pro odběratele, dodavatele nebo obojí.
1. V poli **Počáteční datum / čas** zadejte datum a čas, kdy bude položka k dispozici.
1. V poli **Skupina položky** vyberte skupinu zboží.
1. V polích **Kód 1** až **Kód 10** vyberte kódy filtrů pro omezení položek, které jsou obecně dostupné.

    Při výběru skupiny položek nastavíte tuto skupinu položek veřejně přístupnou. Výběrem kódů filtrů v těchto položkách omezíte obecně dostupné položky.

## <a name="set-up-customer-product-filters"></a>Nastavení filtrů produktů zákazníků

Tato volitelná procedura popisuje postup určení zboží, které má být k dispozici pro odběratele navíc ke zboží, které je dostupné prostřednictvím nastavení filtru na stránce **Obecně dostupné zboží**. Můžete nastavit více filtrů pro jednoho odběratele.

Chcete-li nastavit kódy filtru odběratele, postupujte podle následujících kroků.

1. Přejděte na **Prodej a marketing \> Odběratelé \> Všichni odběratelé**.
1. Vyberte odběratele.
1. V podokně Akce na kartě **Zákazník** ve skupině **Nastavení** zvolte **Filtry produktu**.
1. Na stránce **Kódy filtrů produktu** v podokně Akce vyberte **Nový**.
1. V poli **Počáteční datum / čas** a **Koncové datum / čas** zadejte počáteční a koncové datum pro vybranou skupinu položek.
1. V poli **Skupina položky** vyberte skupinu zboží.
1. V poli **Kód 1** až **Kód 10** vyberte kódy filtrů, které chcete použít jako kritéria k omezení položek, které jsou k dispozici zákazníkům ve vybrané skupině položek. Musíte provést výběr pro každý kód filtru, který je nastaven pro skupinu položek.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Nastavení filtrů produktů dodavatelů

Tato volitelná procedura popisuje postup určení zboží, které má být k dispozici pro dodavatele navíc ke zboží, které je dostupné prostřednictvím nastavení filtru na stránce **Obecně dostupné zboží**. Můžete nastavit více filtrů pro jednoho dodavatele.

Chcete-li nastavit kódy filtru dodavatele, postupujte podle následujících kroků.

1. Přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé**.
1. Vyberte dodavatele.
1. V podokně Akce na kartě **Dodavatel** ve skupině **Nastavení** zvolte **Filtry produktu**.
1. Na stránce **Kódy filtrů** v podokně Akce vyberte **Nový**.
1. V poli **Počáteční datum / čas** a **Koncové datum / čas** zadejte počáteční a koncové datum pro vybranou skupinu položek.
1. V poli **Skupina položky** vyberte skupinu zboží.
1. V poli **Kód 1** až **Kód 10** vyberte kódy filtrů, které chcete použít jako kritéria k omezení položek, které jsou k dispozici dodavatelům ve vybrané skupině položek. Musíte provést výběr pro každý kód filtru, který je nastaven pro skupinu položek.

> [!NOTE]
> Nastavení filtrů produktů dodavatele se vztahuje na vydané produkty, kde jsou pro příslušnou skupinu dimenzí úložiště povoleny procesy správy skladu. Kódy filtru se používají k určení, zda systém umožní uživatelům koupit danou položku od daného dodavatele, když vytvoří řádky nákupní objednávky. Microsoft Dynamics 365 Supply Chain Management má dvě metody pro zacházení se schválením dodavatele. Pokud existuje jeden nebo více vydaných produktů, kde je pole **Schválená metoda kontroly dodavatele** nastaveno na *Pouze varování* nebo *Nepovoleno*, pro tyto položky lze povolit obě metody schválení dodavatele. Tato situace může způsobit problémy, když uživatelé vytvoří řádky nákupní objednávky.

## <a name="see-also"></a>Viz také

[Další informace najdete v příspěvku na blogu WMS-Warehouse Filter Codes](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]