---
title: Vytvoření a konfigurace rozšířených záruk
description: Toto téma popisuje rozšířené záruky a vysvětluje, jak je vytvořit a konfigurovat v aplikaci Microsoft Dynamics 365 Commerce.
author: sijoshi
manager: annbe
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a875343d9b93f5ebf2c2992fba8b2f182310461e
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621186"
---
# <a name="create-and-configure-extended-warranties"></a>Vytvoření a konfigurace rozšířených záruk

[!include [banner](includes/banner.md)]

Toto téma popisuje rozšířené záruky a vysvětluje, jak je vytvořit a konfigurovat v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Zákazníci při nákupu produktů, zejména spotřebního zboží, které se prodává za prémiovou cenu, jako jsou telefony a počítače, stále častěji volí rozšířenou podporu a služby. Poskytnutím rozšířených záruk na nákup mohou maloobchodníci pomoci budovat loajalitu zákazníků. Rozšířené záruky informují zákazníky o tom, kam se mohou obrátit za účelem servisu a podpory. Tím získávají jistotu, že jejich problémy budou řešeny efektivně.

Při prvním nákupu produktu lze zákazníkům v maloobchodním prodejním kanálu prodat rozšířené záruky. Mohou být také prodávány po omezenou dobu po počátečním nákupu.

### <a name="warranty-item-setup"></a>Nastavení záručního zboží

Dynamics 365 Commerce nabízí funkce, které vám umožní vytvořit záruční zbožíku záruky a nastavit pro ni atributy. Mezi tyto atributy patří vztah mezi produktem a záručním zbožím, cena záruky a trvání záruky. Po nakonfigurování a vydání záručního zboží do organizační jednotky může maloobchodník prodávat záruky prostřednictvím moderního prodejního místa (MPOS), online obchodů a dalších maloobchodních kanálů.

### <a name="warranty-item-sales"></a>Prodej záručního zboží

Během počátečního nákupu produktu se zákazníkům v maloobchodním prodejním kanálu prodávají rozšířené záruky. Mohou být také prodávány po omezenou dobu po počátečním nákupu.

V místě prodeje (POS) jsou prodejní partneři vyzváni, aby přidali rozšířenou záruku, když je do košíku zákazníka přidán související produkt. Proto je prodejním partnerům v rámci prodejního toku představena příležitost návazného nebo křížového prodeje.

Zákazníci se také mohou vrátit později a zakoupit si rozšířenou záruku na produkt, který si zakoupili dříve. V těchto případech může obchodní zástupce vyhledat původní transakci a prodat zákazníkovi související zboží s rozšířenou zárukou.

### <a name="warranty-terminology"></a>Terminologie v oblasti záruky

Následující tabulka definuje některé pojmy související se zárukou.

| Termín | popis |
|------------------------------|--------------|
| Rozšířená záruka / záruka | *Rozšířená záruka* označuje na servisní smlouvu nebo smlouvu, která zákazníkům poskytuje prodlouženou záruku. Rozšířená záruka zahrnuje doplňkovou službu výměny nebo opravy zboží během doby krytí rozšířené záruky. |
| Záruka výrobce | *Záruka výrobce* (často označovaná jako *omezená záruka*) je taková záruka, kterou zákazníci obdrží při nákupu produktu. Zde jsou některé funkce záruky výrobce:<ul><li>Záruční náklady jsou zahrnuty v ceně produktu. Zákazníci nemusí za záruku výrobce platit žádnou další částku.</li><li>V závislosti na kategorii produktu záruka výrobce obvykle trvá 30 dní, šest měsíců nebo jeden rok. (U většiny spotřební elektroniky trvá záruka jeden rok).</li><li>Záruka se vztahuje na vady způsobené mechanickými nebo elektrickými poruchami. Pokrytí je omezené a nezahrnuje žádné náhodné poškození zakoupeného produktu. Zákazníci, kteří chtějí chránit nakupované produkty před každodenním poškozením, by měli investovat do rozšířené záruky. Rozšířené záruky trvají dva až deset let v závislosti na kategorii produktu. Mají také širší pokrytí a pokrývají každodenní nehody, jako je upuštění, rozlití a zabarvení.</li></ul> |
| Položka záruky | *Záruční zboží* je zboží s rozšířenou zárukou, které se prodává jako zboží spadající do záruky. Příkladem je dvouletý havarijní plán ochrany notebooků. |
| Zboží spadající do záruky | *Zboží spadající do záruky* je serializovaný produkt, pro který se prodává záruka. Například notebook je zboží spadající do záruky, pro které se prodávají dvouleté a tříleté rozšířené záruky. |
| Skupina záruk | *Skupina záruk* je vtah mezi záručním zbožím a zbožím spadajícím do záruky. POS používá skupiny záruky k určení, na které záruční zboží by měli být prodejní partneři upozorněni, že je vhodné je přidat, když je do košíku zákazníka vloženo zboží spadající do záruky. |
| Zásada záruky | *Záruční podmínky* označují entitu vytvořenou v aplikaci Commerce při prodeji záručních podmínek. Záruční podmínky obsahují informace, jako je počáteční a koncové datum zakoupeného záručního zboží, podmínky a ustanovení a sériové číslo zboží spadajícího do záruky. Čísla záručních podmínek mohou být sdílena se zákazníky, takže mají odkaz na zboží s prodlouženou zárukou, které zakoupili. |

## <a name="create-a-warranty-item"></a>Vytvoření záručního zboží

Chcete-li vytvořit záruční zboží v aplikaci Commerce, postupujte následovně.

1. Přejděte do nabídky **Maloobchodní a velkoobchodní prodej \> Produkty a kategorie \> Produkty**.
1. Zvolte **Nový** pro vytvoření nového záručního zboží.
1. V dialogovém okně **Nový produkt** v poli **Typ produktu** vyberte **Servis**.
1. V poli **Podtyp produktu** vyberte možnost **Produkt**.
1. V poli **Typ servisu produktu** vyberte možnost **Servis**.
1. Do pole **Název produktu** zadejte název produktu.
1. V poli **Kategorie maloobchodu** vyberte hodnotu z rozevíracího seznamu a pak vyberte **OK**.
1. Do pole **Číslo produktu** zadejte číslo produktu.
1. Vyberte **OK**.
1. Na stránce **Detaily produktu** na pevné záložce **Záruka**nastavte hodnoty polí **Jednotka času** a **Doba**.

    | Název pole | Hodnota | popis |
    |------------|-------|-------------|
    | Jednotka času | **Den (dny)**, **Týden (týdny)**, **Měsíc(e)** nebo **Rok(y)** | Toto pole určuje jednotku času, která se používá pro záruku. |
    | Doba | Kladné celé číslo | Toto pole určuje dobu trvání záruky ve vybrané časové jednotce. |

    Například pro dvouletou záruku nastavte hodnotu pole **Jednotka času** na **Rok(y)** a **Doba** na **2**. Případně nastavte hodnotu v poli **Jednotka času** na **Měsíc(e)** a hodnotu v poli **Doba** na **24**, jak ukazuje následující obrázek.

    ![Stránka s podrobnostmi o produktu pro záruční zboží](./media/ew-time-properties.png)

1. Kliknutím na tlačítko **Uložit** uložte záruční zboží.
1. Vydejte záruční produkt společnosti, aby mohl být prodán. Další informace získáte v tématu [Nastavení maloobchodních produktů](set-up-retail-products.md)
1. Na stránce **Podrobnosti o vydaném produktu** na pevné záložce **Záruka** nastavte hodnoty polí **Základ cenového rozsahu**, **Dolní limit** a **Horní limit**.

    | Název pole | Hodnota | popis |
    |------------|-------|-------------|
    | Základ cenového rozsahu | **Žádná**, **Základní cena** nebo **Prodejní cena** | <ul><li>**Žádná** - Hodnoty **Dolní limit** a **Horní limit** hodnoty cenových rozsahů nejsou aplikovatelné.</li><li>**Základní cena** – Daná záruka bude uplatněna, pokud bude základní cena (tj. cena bez slev) u zboží spadajícího do záruky mezi hodnotami **Dolní limit** a **Horní limit**, které jsou zde specifikovány, na základě ceny zboží spadajícího do záruky.</li><li>**Prodejní cena** - Tato hodnota je vyhrazena pro budoucí použití.</li></ul> |
    | Dolní limit, Horní limit | Kladné celé číslo | Tato pole definují horní a dolní cenové limity zboží spadajícího do záruky a způsob, jakým je aktuální záruční zboží aplikovatelné na zboží spadající do záruky. Tyto limity mohou být založeny na základní ceně zboží spadajícího do záruky (známé také jako maloobchodní cena doporučená výrobcem) \[MSRP\]). Pokud je hodnota v poli **Základ cenového rozpětí** nastavena na **Základní cena**, bude pouze zboží spadající do záruky (produkt) se základní cenou mezi hodnotou **Dolní limit** a **Horní limit** vyvolávat výzvu k přidání záručního zboží do POS. |

    Například následující obrázek ukazuje pole **Základ cenového rozpětí** nastavené na hodnotu **Základní cena**, pole **Dolní limit** nastavené na $500 a pole **Horní limit** nastavené na $1000.
    
    ![Stránka s podrobnostmi o vydané produktu pro záruční zboží](./media/ew-release-product-details.png)

1. Zařaďte záruční zboží do kanálu, kde bude prodáváno. Další informace naleznete v tématu [Nastavení sortimentu](set-up-assortments.md).

### <a name="example"></a>Příklad

Záruční zboží ve formě notebooku (produkt) má základní cenu $999 a existují dvě záruční zboží pro notebook:

- Záruka\_1 má dolní limit $500 a horní limit $1000 a v poli **Základ cenového rozpětí** je nastavena hodnota **Základní cena**.
- Záruka\_2 má dolní limit $1,001 a horní limit $2,000 a v poli **Základ cenového rozpětí** je nastavena hodnota **Základní cena**.

V tomto případě, když je do košíku zákazníka přidán notebook jako zboží spadající do záruky, v POS se zobrazí výzva k přidání Záruky\_1, protože cena notebooku je mezi dolním a horním limitem pro záruku\_1.

> [!NOTE]
> V tomto příkladu, pokud chcete zobrazit výzvu pro záruku\_1 i záruku\_2 bez ohledu na cenu zboží spadajícího do záruky, nastavte hodnotu v poli **Základ cenového rozpětí** na **Žádný**.

## <a name="configure-channel-specific-settings"></a>Konfigurace nastavení specifických pro kanál

Nastavení specifická pro daný kanál vám umožňují určit, zda se má v POS zobrazit výzva k přidání záručního zboží, když je do košíku zákazníka přidáno zboží spadající do záruky.

Chcete-li nakonfigurovat nastavení specifické pro kanál v aplikaci Commerce, proveďte následující postup.

1. Přejděte na **Retail and Commerce \> Produkty a kategorie \> Záruka \> Nastavení záruky**.
1. Na kartě **Specifické pro kanál** ve sloupci **Výzva pro záruku** proveďte pro svůj kanál jeden z těchto kroků:

    - Zaškrtněte políčko, pokud se má v POS při zobrazení zboží spadajícího do záruky zobrazit výzva pro záruční zboží.
    - Zaškrtněte políčko, pokud se v POS při zobrazení zboží spadajícího do záruky nemá zobrazit výzva pro záruční zboží.

1. Spusťte úlohu **1070** k synchronizaci dat v kanálu.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Konfigurace číselné řady pro záruční podmínky

Každé záruční podmínky jsou jednoznačně identifikovány číslem záručních podmínek, které je generováno číselnou řadou. Další informace o číselných řadách naleznete v tématu [Přehled číselných řad](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Chcete-li nakonfigurovat číselnou řadu pro záruční podmínky v aplikaci Commerce, postupujte takto.

1. Přejděte na **Retail and Commerce \> Produkty a kategorie \> Záruka \> Nastavení záruky**.
1. Na kartě **Číselné řady** na řádku reference **Záruční podmínky** zadejte nebo vyberte hodnotu v poli **Kód číselné řady**.

## <a name="set-up-a-warranty-group"></a>Nastavení skupiny záruk

Skupina záruk je vtah mezi záručním zbožím a zbožím spadajícím do záruky. POS používá skupiny záruky k určení, na které záruční zboží by měli být prodejní partneři upozorněni, že je vhodné je přidat, když je do košíku zákazníka vloženo zboží spadající do záruky.

Chcete-li nastavit skupinu záruk v aplikaci Commerce, postupujte podle následujících pokynů.

1. Přejděte na **Retail and Commerce \> Produkty a kategorie \> Záruka \> Skupiny záruky**.
1. Zvolte **Nový** pro vytvoření nové skupiny záruk.
1. Do pole **Název** zadejte název nové skupiny.
1. Na pevné záložce **Obecné** v poli **Popis** zadejte popis skupiny.
1. Na pevné záložce **Produkty záruky** vyberte **Přidat řádek** pro přidání záručního zboží.
1. Do pole **Pořadí řazení** zadejte číslo pro zařazení skupiny záruk v POS. POS zobrazí záruční zboží ve vzestupném pořadí ve výzvě k záruce.
1. Na pevné záložce **Produkty spadající do záruky** vyberte **Přidat řádek** pro přidání produktů spadajících do záruky.
1. Pokud je záruční zboží použitelná pro celou kategorii zboží (produktů) spadajícího do záruky, vyberte kategorii v poli **Kategorie**. Pokud je záruční zboží použitelné u konkrétního zboží (produktu) spadajícího do záruky, vyberte produkt v poli **Produkt**.
1. Na pevné záložce **Použitelné kanály** vyberte **Přidat řádek** pro přidání kanálu, ve kterém chcete záruční zboží prodávat.
1. Výběrem tlačítka **Uložit** konfiguraci uložte.
1. Výběrem možnosti **Publikovat** publikujte skupinu záruky.
1. Spusťte úlohu **1040** k synchronizaci dat v kanálu.

## <a name="sell-warranty-items-at-the-pos"></a>Prodej záručního zboží v POS

Dvě operace POS umožňují prodejním partnerům prodávat během pracovního postupu záruční zboží jako nákupy zákazníků:

- **Přidat záruku** - Tato operace spustí výzvu, která ukazuje použitelné záruky na zboží spadající do záruky, které je vybráno v košíku.
- **Přidat záruku k existující transakci** - Tato operace umožňuje prodejním partnerům prodávat záruky pro zboží spadající do záruky, které bylo prodáno předtím. Prodejní partneři mohou najít původní transakci pro zboží spadající do záruky zadáním čísla příjmu transakce.

Následující obrázek ukazuje příklad stránky terminálu POS s výzvou k přidání záručního zboží u zboží spadajícího do záruky.

![Příklad výzvy k přidání záručního zboží pro aktuální nákup](./media/ew-sell-warranty.png)

Následující obrázek ukazuje příklad funkce pro přidání záručního zboží u zboží spadajícího do záruky, které bylo přidáno předtím.

![Příklad funkce pro přidání záručního zboží pro dříve prodané zboží spadající do záruky](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Zpracovat transakce záruky

Pokud jsou záruky prodávány v transakcích cash-and-carry mohou po zaúčtování transakcí v centrálách aplikace Commerce uživatelé této aplikace spustit úlohu **Zpracovat transakce záruky** ke zpracování transakcí záruky a vytvoření záručních podmínek.

Při zpracování transakcí záruky v centrále aplikace Commerce postupujte následovně.

1. Přejděte na **Retail and Commerce \> Produkty a kategorie \> Záruka \> Zpracovat transakce záruky**.
1. V dialogovém okně **Zvolit uzly organizace** v poli **Hierarchie organizace** vyberte hodnotu.
1. V seznamu **Dostupné uzly organizace** vyberte jednotlivé úložiště nebo, chcete-li vytvořit dávkovou úlohu pro skupinu obchodů, vyberte uzel.
1. Výběrem tlačítka se šipkou doprava přidejte výběr do seznamu **Vybrané uzly organizace**.
1. Vyberte kartu **Spustit na pozadí**.
1. Nastavte možnost **Dávkové zpracování** na **Ano** a pak vyberte **Opakování**.
1. V dialogovém okně **Definovat opakování** v poli **Počáteční datum** vyberte nebo zadejte počáteční datum opakování.
1. V poli **Počáteční čas** vyberte nebo zadejte počáteční čas pro opakování.
1. Proveďte jeden z následujících kroků:

    - Pokud nemá opakování skončit, vyberte možnost **Žádné datum ukončení**.
    - Pokud má opakování skončit po konkrétním počtu spuštění, vyberte možnost **Konec po**. Pokud vyberete tuto možnost, zadejte počet spuštění.
    - Pokud má opakování skončit do konkrétního data, vyberte možnost **Ukončit do**. Pokud vyberete tuto možnost, vyberte nebo zadejte datum.

1. Vyberte **OK**.
1. Vyberte **OK**.

## <a name="warranty-policies"></a>Záruční podmínky

Při prodeji rozšířené záruky se automaticky vytvoří entita záručních podmínek. Čísla záručních podmínek mohou být sdílena se zákazníky, takže mají odkaz na záruční zboží, které zakoupili. Mezi vlastnosti záručních podmínek patří datum zahájení a ukončení platnosti záruky, smluvní podmínky a sériové číslo zboží spadajícího do záruky, za které byla záruka prodána.

> [!NOTE]
> Vlastnosti záručních podmínek se generují automaticky při vytváření entit záručních podmínek. V současné době je nelze ručně konfigurovat ani upravovat.

Následující tabulka popisuje vlastnosti záručních podmínek a jejich hodnoty. V centrále aplikace Commerce se tabulka databáze jmenuje WARRANTYPOLICY.

| Název vlastnosti | Hodnota | popis |
|---------------|-------|-------------|
| PolicyNumber | Řetězec znaků (maximálně 20 znaků) | Číslo záručních podmínek |
| WarrantiedItemId | Řetězec znaků (maximálně 20 znaků) | ID zboží spadajícího do záruky |
| WarrantiedInventoryLotId | Řetězec znaků (maximálně 20 znaků) | ID šarže zboží spadajícího do záruky |
| WarrantiedSerialNumber | Řetězec znaků (maximálně 20 znaků) | Sériové číslo zboží spadajícího do záruky. |
| WarrantiedFulfilledDate | Datum | Datum plnění zboží spadajícího do záruky |
| WarrantyItemId | Řetězec znaků (maximálně 20 znaků) | ID záručního zboží |
| WarrantyInventoryLotId | Řetězec znaků (maximálně 20 znaků) | ID šarže záručního zboží |
| WarrantySalesDate | Datum | Datum prodeje záručního zboží |
| WarrantyEffectiveDate | Datum | Datum účinnosti záručních podmínek |
| WarrantyExpirationDate | Datum | Datum vypršení platnosti záručních podmínek |
| CustAccount | Řetězec znaků (maximálně 20 znaků) | Číslo účtu odběratele |
| Stav | **Vytvořeno**, **Zrušeno**, **Platné** nebo **S vypršenou platností** | Stav záručních podmínek |
| Poznámky | Řetězec znaků (maximálně 255 znaků) | Poznámky k záručním podmínkám, jako jsou smluvní podmínky |

## <a name="frequently-asked-questions-faq"></a>Časté dotazy

**Proč v POS nevidím výzvu k záruce?**

Ujistěte se, že je položka záruky přiřazena kanálu. Také se ujistěte, že skupina záruk je nakonfigurována tak, aby obsahovala příslušný kanál.

**Když se pokusím přidat záruku k existující transakci a zadat číslo potvrzení objednávky zákazníka, proč nevidím žádné řádkové položky transakce?**

Účtenky lze najít, pouze pokud je spuštěna úloha vyžádání (P-úloha) k nahrání účtenek do centrály Commerce. Pokud chcete spustit P-úlohu, přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**, vyberte úlohu **P-0001** a pak vyberte **Spustit**.

**Proč se záruka vztahuje pouze na serializované produkty?**

Záruka je služba poskytovaná pro konkrétní jedinečný produkt. V Dynamics 365 lze produkt jednoznačně identifikovat pouze sériovým číslem.

## <a name="additional-resources"></a>Další prostředky

[Nastavení maloobchodních produktů](set-up-retail-products.md)

[Nastavení sortimentu](set-up-assortments.md)

[Přehled číselných řad](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)
