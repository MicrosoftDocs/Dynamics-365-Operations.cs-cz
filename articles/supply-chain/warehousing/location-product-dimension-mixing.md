---
title: Směšování dimenzí produktu na skladovém místě
description: Toto téma poskytuje informace o míchání dimenzí produktů na skladovém místě. Tato funkce profilu skladového místa pomáhá zlepšit správu skladového místa, pokud se používají varianty produktu nebo produkty, které mají různé dimenze, jako například v módním průmyslu. Funkce umožní rozhodnout, zda je možné konfigurace, barvy, styly a velikosti pro konkrétní profil skladového místa míchat, nebo zda lze na jedno skladové místo umístit pouze jednu dimenzi nebo kombinaci.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 031b92f827979c01dbf0208ba21ae827fb13920b
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103481"
---
# <a name="location-product-dimension-mixing"></a>Směšování dimenzí produktu na skladovém místě

[!include [banner](../includes/banner.md)]

Míchání dimenzí produktu na skladovém místě je funkce profilu skladového místa, jež pomáhá zlepšit správu skladového místa, pokud se používají varianty produktu nebo produkty, které mají dimenze, jako například v módním průmyslu. Funkce umožní rozhodnout, zda je možné konfigurace, barvy, styly a velikosti pro konkrétní profil skladového místa míchat, nebo zda lze na jedno skladové místo umístit pouze jednu dimenzi nebo kombinaci.

## <a name="turn-the-location-product-dimension-mixing-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce míchání dimenzí produktů na skladovém místě

Chcete-li používat funkčnost popsanou v tomto tématu, musí být ve vašem systému zapnuta funkce *Směšování dimenzí produktu na skladovém místě*. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Směšování dimenzí produktu na skladovém místě* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>Nastavení

Každé skladové místo ve skladu musí mít přidružený profil skladového místa, který popisuje vlastnosti skladového místa. Na všech skladových místech, jež používají stejný profil skladového místa, proto bude možné po nastavení využívat míchání dimenzí produktů na skladovém místě.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Konfigurace profilů skladových míst, aby umožňovaly míchání dimenzí produktů

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. V seznamu profilů polohy vyberte možnost **HROMADNĚ**.
1. V podokně akcí vyberte **Upravit**.
1. Na záložce s náhledem **Všeobecné** nastavte u položky **Povolit míchání dimenzí produktu na skladovém místě** hodnotu *Ano*.

    > [!NOTE]
    > U této možnosti můžete nastavit hodnotu *Ano*, pouze když je u možnosti **Povolit míchání položek** nastavena možnost *Ne*.

1. Na záložce s náhledem **Povolit míchání položek** nastavte u položky **Velikost** hodnotu *Ano*. Ve scénáři popsaném v tomto tématu lze míchání provádět pouze u produktů, které se liší dimenzí **Velikost**. K dispozici jsou však také další možnosti.
1. Zvolte **Uložit**.

### <a name="create-a-new-product-master-and-product-variants"></a>Vytvoření nového základního produktu a variant produktů

1. Přejděte do nabídky **Řízení informací o produktech \> Produkty \> Základní produkty**.
1. V podokně akcí vyberte možnost **Nový** a vytvořte základní produkt.
1. V dialogovém okně **Nový produkt** nastavte následující hodnoty:

    - **Typ produktu:** *Položka*
    - **Podtyp produktu:** *Základní produkt*
    - **Číslo produktu:** *B0001*
    - **Název produktu:** *B0001 Velikost*
    - **Skupina dimenzí produktů:** *Velikost*
    - **Konfigurační technologie:** *Předdefinovaná varianta*

1. Vyberte **OK**.
1. Na stránce **Podrobnosti produktu** nastavte na záložce s náhledem **Všeobecné** následující hodnoty:

    - **Automaticky generovat varianty:** *Ano*
    - **Velikostní skupina:** *CASUALDHIR*

1. Chcete-li zobrazit předdefinované varianty, vyberte v podokně Akce možnost **Varianty produktu**.

    Zobrazí se stránka **Varianty produktu** a na ní seznam variant z konfigurace velikostní skupiny.

### <a name="release-products-to-the-usmf-company"></a>Uvolnění produktů společností USMF

1. V podokně Akce vyberte možnost **Uvolnit produkty**.
1. Na stránce **Výběr produktů k uvolnění** si zkontrolujte, že je produkt číslo *B0001* v seznamu, poté vyberte možnost **Další**.
1. Výběrem možnosti **Další** potvrzujete varianty produktu k uvolnění.
1. Na stránce **Výběr společností k uvolnění** vyberte možnost *USMF*, poté výběr potvrďte kliknutím na **Další**.
1. Na stránce **Potvrzení výběru** klikněte na **Dokončit**, tím se uvolnění dokončí.

    Zobrazí se zpráva „Operace dokončena“.

### <a name="update-a-released-product-in-the-usmf-company"></a>Aktualizace uvolněného produktu ve společnosti USMF

1. Ujistěte se, že jste přihlášeni do společnosti **USMF**.
1. Přejděte do **Řízení informací o produktech \> Produkty \> Uvolněné produkty**, vytváření uvolněného produktu se dokončí.
1. Najděte a vyberte položku číslo *B0001*. Otevřete stránku **Podrobnosti uvolněného produktu**.
1. V podokně akcí vyberte **Upravit**.
1. Na záložce s náhledem **Všeobecné** se ujistěte, že je v poli **Skupina modelů položek** zadána hodnota *FIFO*.
1. V podokně Akce na kartě **Produkt** ve skupině **Nastavení** zvolte **Skupiny dimenzí**.
1. Nastavte následující hodnoty:

    - **Skupina dimenze úložiště:** *Ware*
    - **Skupina sledovací dimenze:** *Žádná*

1. Vyberte **OK**.
1. V podokně Akce na kartě **Produkt** ve skupině **Nastavení** zvolte **Hierarchie rezervací**.
1. Nastavte v poli **Hierarchie rezervací** hodnotu *Výchozí*, poté klikněte na **OK**.
1. Na záložce s náhledem **Všeobecné** si v části **Správa** všimněte, že byl výběr aktualizován.
1. Na záložce s náhledem **Nákup** zadejte do pole **Cena** hodnotu *10*.
1. Na záložce s náhledem **Řízení nákladů** zadejte do pole **Skupina položek** hodnotu *Audio*.
1. Na záložce s náhledem **Nákup** zadejte do pole **Cena** hodnotu *10*.
1. Na záložce s náhledem **Sklad** zadejte v poli **ID skupiny pořadí jednotek** hodnotu *ks*.
1. Zvolte **Uložit**.

### <a name="create-a-location-directive"></a>Vytvoření směrnice skladového místa

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně vyberte v poli **Typ pracovního příkazu** hodnotu *Nákupní objednávky*.
1. V seznamu vyberte směrnici skladového místa, jež se jmenuje *24 PO Direct*.
1. Na záložce s náhledem **Akce směrnice skladového místa** přidejte řádek do mřížky výběrem možnosti **Nová**.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** *1*

        Nový řádek by měl být před již dříve existujícím řádkem. Chcete-li provést změnu, použijte tlačítka **Pohyb nahoru** a **Pohyb dolů** na panelu nástrojů nebo změňte hodnotu v poli **Pořadové číslo** stávajících řádků na *2*.

    - **Název:** *Vložení do profilu skladového místa BULK*
    - **Využití pevného skladového místa:** *Pevná a nepevná skladová místa*
    - **Povolit záporný stav zásob:** *Zrušte zaškrtnutí tohoto políčka (= Ne)*
    - **Dávka povolena:** *Zrušte zaškrtnutí tohoto políčka (= Ne)*
    - **Strategie:** *Žádná*

1. Dokud je ještě nový řádek vybrán, klikněte na **Upravit dotaz** nad mřížkou.
1. V dialogovém okně dotazu na kartě **Oblast** přidejte tlačítkem **Přidat** nový řádek mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *umístění*
    - **Odvozená tabulka:** *Skladová místa*
    - **Pole:** *ID profilu skladového místa*
    - **Kritéria:** *BULK*

1. Vyberte **OK**.
1. Na stránce **Směrnice skladového místa** v podokně Akce vyberte **Uložit**.

> [!NOTE]
> Na záložce s náhledem **Akce směrnice skladového místa** v poli **Strategie**: pokud používáte strategii skladových míst *Konsolidace*, bude nastavení na záložce s náhledem **Povolit míchání dimenzí produktů** na stránce **Profily skladových míst** přepsáno a položky budou ukládány do stejného skladového místa, i když nastavení takové chování nepovoluje.

### <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně Akce vyberte možnost **Nová**, vytvoří se položka nabídky, jež se bude používat k třídění.
1. V záhlaví nastavte následující hodnoty:

    - **Název položky nabídky:** *Příjem řádku PO*
    - **Název:** *Příjem řádku PO*
    - **Režim:** *Práce*
    - **Použít existující práci:** *Ne*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Proces tvorby práce:** *Příjem a vyskladnění řádku nákupní objednávky*
    - **Generovat registrační značky:** *Ano*

1. Zvolte **Uložit**.

### <a name="configure-the-mobile-device-menu"></a>Proveďte konfiguraci nabídky mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V seznamu nabídek vyberte možnost **Vstupní**.
1. V podokně akcí vyberte **Upravit**.
1. V seznamu **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky **Příjem řádku PO**.
1. Stisknutím tlačítka se šipkou doprava přesuňte položku nabídky **Příjem řádku PO** do seznamu **Struktura nabídky**. Tímto způsobem se přidá nová položka nabídky do vybrané nabídky.
1. Zvolte **Uložit**.

## <a name="scenario"></a>Scénář

Tento ukázkový scénář demonstruje, jak lze umístit dvě různé varianty produktu na stejné skladové místo, když profil skladového místa neumožňuje směšování položek, ale je povolena funkce *Směšování dimenzí produktu na skladovém místě*. V tomto případě využijeme jako kritérium variantu **velikosti**.

Než začnete, ujistěte se, že jsou ve skladu *24* prázdná místa, jež využívají profil skladového místa *BULK*.

### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

Vytvoříte nákupní objednávku, která má tři řádky: dva řádky pro stejné číslo produktu, ale v odlišné variantě **Velikost**, třetí řádek bude pro jiný produkt, který nemá varianty.

1. Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:

    - **Účet dodavatele:** *1001*
    - **Sklad:** *24*

1. Vyberte **OK**.
1. Vytvoří se nákupní objednávka a na záložce s náhledem **Řádky nákupní objednávky** bude přidán nový řádek. Poznamenejte si číslo nákupní objednávky.
1. Na novém řádku nastavte následující hodnoty:

    - **Číslo položky:** *B0001*
    - **Velikost** *L*
    - **Množství:** *2*

1. Chcete-li přidat druhý řádek objednávky, klikněte na položku **Přidat řádek** nad mřížkou a nastavte následující hodnoty:

    - **Číslo položky:** *B0001*
    - **Velikost** *XL*
    - **Množství:** *2*

1. Chcete-li přidat třetí řádek nákupní objednávky, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *1*

1.Zvolte **Uložit**.

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a>Přijetí řádků objednávky v mobilní aplikaci Řízení skladu

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel, který má povolen sklad *24*.
1. Vyberte nabídku **Vstupní**.
1. Vyberte **Příjem řádku PO**.
1. Vyberte pole **ČÍSLOPO** a zadejte číslo nákupní objednávky.
1. Zadání potvrďte výběrem tlačítka pro potvrzení (✔) ve spodní části stránky.
1. Zadejte číslo řádku z nákupní objednávky, kterou přijímáte. Vyberte pole **ČÍSLOŘÁDKU** a poté zadejte pomocí číselné klávesnice hodnotu *1*.
1. Potvrďte zadání.
1. Zadejte přijímané množství. Klikněte dvakrát na tlačítko se znaménkem plus (**+**). Zvýšíte tím hodnotu v poli **Množ.** na *2*.
1. Zaregistrujte záznam stiskem tlačítka (✔) v dolní části stránky a poté zadání potvrďte opětovným stisknutím tlačítka (✔).
1. Prohlédněte si informace na stránce **Nákupní objednávky: zaskladnění**. Tato stránka zobrazuje práci, která byla vytvořena pro zaskladnění (Práce 1).

    Pro právě dokončený **Příjem řádku PO** se zobrazí místo, kam bude přijatá položka umístěna, registrační značka, položka, velikost a množství.

1. Potvrďte práci zaskladnění.
1. Opakujte kroky 4 až 11 pro řádek 2 objednávky. V kroku 8 však zadejte množství *1*.

    Nová práce zaskladnění (práce 2) bude vytvořena pro stejné skladové místo jako práce 1.

1. Znovu opakujte kroky 4 až 11 pro řádek 2 objednávky. V kroku 8 zadejte zbývající množství *1*.

    Nová práce zaskladnění (práce 3) bude vytvořena pro stejné skladové místo jako práce 1 a práce 2. Toto chování je způsobeno tím, že se používá strategie směrnice skladového místa *Konsolidovat* a protože záložka s náhledem **Povolit míchání položek** v **profilu skladového místa** *Hromadně* umožňuje na skladovém místě míchat varianty **velikosti**.

1. Opakujte kroky 4 až 11 pro řádek 3 objednávky. V kroku 8 zadejte pro položku číslo *A0001* množství *1*.

    Nová zaskladňovací práce (práce 4) se vytvoří pro jiné skladové místo než to, jež se použilo pro řádky 1 a 2 objednávky. K tomuto chování dochází, protože profil skladového místa neumožňuje míchání produktů, ale umožňuje míchání dimenzí stejného základního produktu.

1. Stiskněte tlačítko nabídky v horní části stránky (tzv. „hamburgerové tlačítko“ nebo „hamburger“) a vyberte **Storno**, chcete-li **Příjem řádku PO** opustit.

> [!TIP]
> Tento scénář můžete opakovat, ale tentokrát nastavte **Velikost** - *Ne* na záložce s náhledem **Povolit míchání dimenzí produktu** v **profilu skladového místa** *BULK*. V takovém případě nebude možné dimenze produktů míchat. V tomto případě bude po obdržení nákupní objednávky každá varianta produktu umístěna na nové skladové místo.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]