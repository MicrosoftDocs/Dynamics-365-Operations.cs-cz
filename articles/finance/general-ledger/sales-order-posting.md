---
title: Zaúčtování prodejní objednávky
description: Toto téma obsahuje informace o kartě Prodejní objednávka na stránce profilu zaúčtování zásob.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5d84723b51d6977867fa162c4a47befa61bd9ef6
ms.sourcegitcommit: dc3053625dfe24aef64399dd1d002214e7f7619f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755921"
---
# <a name="sales-order-posting"></a>Zaúčtování prodejní objednávky

Karta **Prodejní objednávka** na stránce **Profily zaúčtování zásob** se používá ke kontrole toho, jak se prodejní objednávky zaúčtují do hlavní knihy. Do hlavní knihy pro prodejní zakázku jsou zaúčtovány dvě hlavní činnosti: 

- Dodací list
- Faktura

Pro zaúčtování fyzické transakce (dodací list) do hlavní knihy pro prodejní objednávku musí být splněny následující podmínky:

- Na stránce **Parametry řízení zásob a skladu** musí být zaškrtnuto políčko **Zaúčtovat dodací list do účetní knihy**.
- Na stránce **Modelová skupina položek** pro položku vybranou na řádku prodejní objednávky musí být zaškrtnuto políčko **Zaúčtovat fyzické zásoby do účetní knihy**.
- Na stránce **Profil účtování zásob** musí být uvedeny hlavní účty pro následující typy zaúčtování:
  - Náklady jednotek, dodané
  - Náklady prodaného zboží, dodané

Pro zaúčtování finanční transakce (faktura) do hlavní knihy pro prodejní objednávku musí být splněny následující podmínky:

- Na stránce **Modelová skupina položek** pro položku vybranou na řádku prodejní objednávky musí být zaškrtnuto políčko **Zaúčtovat finanční zásoby do účetní knihy**.
- Hlavní účet musí být uvedený na stránce **Profil účtování zásob** pro následující typy zaúčtování:
  - Náklady jednotek, fakturované
  - Náklady prodaného zboží, fakturované
  - Výnosy
  - Sleva\*

> [!NOTE]
> Slevový účet je volitelný. Mnoho účetních předpisů, jako jsou GAAP a IFRS, vyžaduje, aby slevy snižovaly tržby z prodeje, a proto se tyto účty v mnoha scénářích nepoužívají. Pokud to místní předpisy umožňují, použijte k zaúčtování části prodejní ceny, která je zlevněna, samostatný hlavní účet.

Chcete-li zaúčtovat hodnotu odložených (odhadovaných) výnosů do hlavní knihy při generování dodacího listu pro prodejní objednávku, musí být splněny následující podmínky:

- Na stránce **Modelová skupina položek** pro položku vybranou na řádku prodejní objednávky musí být zaškrtnuto políčko **Zaúčtovat fyzické zásoby do účetní knihy**.
- Na stránce **Modelová skupina položek** musí být zaškrtnuto políčko **Zaúčtovat na účet odložených příjmů při doručení prodeje**.
- Na stránce **Parametry řízení zásob a skladu** musí být zaškrtnuto políčko **Zaúčtovat dodací list do účetní knihy**.
- Na stránce **Parametry řízení zásob a skladu** musí být zaškrtnuto políčko **Zaúčtovat fyzickou DPH**.
- Na stránce **Parametry pohledávek** musí být zaškrtnuto políčko **Zaúčtovat dodací list do účetní knihy**.
- Na stránce **Profil účtování zásob** musí být uvedeny hlavní účty pro následující typy zaúčtování:
  - Odložený výnos při dodání
  - Protiúčet odloženého výnosu při dodání
  - Odložená DPH při dodání

> [!NOTE]
> Obecně doporučujeme povolit možnosti **Zaúčtujte fyzické zásoby** a **Zaúčtovat dodací list do účetní knihy**. Povolení těchto možností může pomoci urychlit postupy uzavírání na konci měsíce, protože nebude nutné ručně počítat a účtovat žádné odklady. Kromě toho budou finanční výkazy odrážet odložené částky automaticky bez ručního zásahu.

> [!IMPORTANT]
> Možnost **Zaúčtovat na účet odložených příjmů při doručení prodeje** se nepoužívá pro účtování výnosů. Další informace o uznávání příjmů naleznete na [Přehled účtování tržeb](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Ukázka konfigurace profilu zveřejňování 

Následující tabulka ukazuje příklady výchozích typů účtování s ukázkovými hlavními účty a popisy:
 
- Sloupec **Clearingový účet** označuje, že typ účtování je clearingový účet. Částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce. 
- Sloupec **P/F** označuje **P** pro fyzické zaúčtování a **F** pro finanční zaúčtování. 
- Sloupec **Sledovat** udává, zda je hlavní účet pro určitý typ účtování obvykle stejný jako jiný typ účtování. Hodnota ve sloupci označuje typ účtování, který se obvykle používá.

> [!NOTE]
> Tyto hlavní účty a názvy hlavních účtů jsou pouze návrhy. Doporučujeme, abyste ve spolupráci se svým účetním určili nejlepší konfiguraci pro vaše obchodní potřeby.


| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Má dáti/Dal? | Clearingový účet | P/F | Sledovat | Popis |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Náklady jednotek, dodané | 140100</br>140101 | Zásoby materiálů</br>Expedované nefakturované materiály | Materiál | Kredit | Ano | P | Náklady jednotek, fakturované | Používá se, když je zaúčtován dodací list prodejní objednávky. Protiúčet je Náklady prodaného zboží, dodané. Částka na tomto účtu je stornována při zaúčtování faktury prodejní objednávky. Možná budete chtít použít účet Expedované nefakturované materiály k reprezentaci fyzické zásoby a rezervovat účet Zásoby materiálů pro finanční aktualizaci. |
| Náklady prodaného zboží, dodané | 500150 | Odložené COGS | Výdaje | Debet | Ano | P  | Používá se, když je zaúčtován dodací list prodejní objednávky. Protiúčet je Náklady jednotek, dodané. Částka na tomto účtu je stornována při zaúčtování faktury prodejní objednávky. |
| Náklady jednotek, fakturované | 140100 | Zásoby materiálů | Materiál | Kredit | Číslo | F | Náklady jednotek, dodané | Používá se, když je zaúčtována faktura prodejní objednávky. Protiúčet je Náklady prodaného zboží, fakturované. Tento účet představuje zásoby ve vaší rozvaze. |
| Náklady prodaného zboží, fakturované | 500100 | Materiály COGS | Výdaje | Debet | Číslo | F  | Používá se, když je zaúčtována faktura prodejní objednávky. Protiúčet je Náklady jednotek, fakturované. Tento účet představuje COGS na vašem výkazu P&amp;L. |
| Výnosy (výnosy z prodejní objednávky*) | 400100 | Výnosy materiálů | Výnosy | Kredit | Číslo | F   | Používá se, když je zaúčtována faktura prodejní objednávky. Protiúčet k tomuto účtu je Součtový účet (zůstatek zákazníka*) na **Profilu zaúčtování pohledávek**. |
| Provize (Prodeje, provize*) | 602150 | Výdaj na provizi | Výdaje | Debet | Číslo | F  | Používá se, když je provize povolena a vypočtena pro prodej a zaúčtována během procesu fakturace prodejní objednávky. Protiúčet pro tento účet je Závazek z provize. |
| Protiúčet provize (prodej, protiúčet provize*) | 201110 | Provize – závazky | Pasiva | Kredit | Ano | F | Používá se, když je provize povolena a vypočtena pro prodej a zaúčtována během procesu fakturace prodejní objednávky. Protiúčet pro tento účet je Výdaj z provize. |
| Odložený výnos při dodání (prodej – výnos z dodacího listu*) | 401400 | Časově rozlišené tržby | Výnosy | Kredit | Ano | P  | Používá se, když je povoleno Odložený výnos při dodání a je zaúčtováno, když zpracováváte dodací list prodejní objednávky. Protiúčtem je Protiúčet odloženého výnosu. Částky na tomto účtu jsou automaticky stornovány při zaúčtování faktury prodejní objednávky. |
| Protiúčet odloženého výnosu při dodání (prodej – protiúčet výnosu z dodacího listu)* | 130400 | Pohledávky – nefakturováno | Materiál | Debet | Ano | P  | Používá se, když je povoleno Odložený výnos při dodání a je zaúčtováno, když zpracováváte dodací list prodejní objednávky. Protiúčtem je Odložený výnos při dodání. Částky na tomto účtu jsou automaticky stornovány při zaúčtování faktury prodejní objednávky. |
| Odložené DPH při dodání (prodej, daň z dodacího listu*) | 250500 | Odložená DPH | Pasiva | Kredit | Ano | P  | Používá se, když je povolen Odložený výnos při dodání a je povoleno Zaúčtovat fyzickou DPH. Částka daně je zaúčtována, když zpracováváte dodací list prodejní objednávky. |

\*Hodnoty uvedené v závorkách v této tabulce představují hodnotu, která je použita v poli **Typ zaúčtování** na stránce **Transakce dokladu**. Můžete zobrazit **Typ účtování** na stránce **Transakce dokladů** na kartě **Všeobecné**.

## <a name="sales-category-posting"></a>Zaúčtování prodejní kategorie

Jako alternativu k nastavení účtování zásob pro všechny položky, skupinu položek nebo jednu položku můžete nastavit kategorie a řídit účtování v hlavní knize podle kategorií prodeje. Další informace o nastavení hierarchie kategorií a přiřazení kategorií k produktům naleznete na [Vytvořte hierarchii klasifikace produktů](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) a [Klasifikujte produkt pomocí hierarchií kategorií](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Po vytvoření hierarchie kategorií musíte hierarchii přiřadit k jednomu nebo více typům. Chcete-li u prodejních objednávek použít hierarchii kategorií, musíte kategorii přiřadit k typu hierarchie prodejní kategorie. Další informace naleznete v [Informacích o hierarchii kategorií](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Zaúčtování tvorby výnosů dle kategorie prodeje

Chcete-li přiřadit účtování hlavní knihy pro prodejní objednávku na základě prodejní kategorie, postupujte takto:

1. Přejděte na **Řízení zásob** > **Nastavení** > **Zaúčtování** > **Zaúčtování**.
2. Vyberte kartu **Prodej**.
3. Vyberte přepínač pro typ účtování, který chcete konfigurovat (např. **Výnosy**).
4. Zvolte **Nové**.
5. V poli **Kód položky** vyberte **Kategorie**.
6. Použijte pole **Vztah kategorií** a vyberte kategorii pro účetní profil.
7. V poli **Kód účtu** vyberte možnost pro **Tabulku**, **Skupinu** nebo **Vše**. Chcete-li například profil účtování použít pro všechny zákazníky, vyberte **Vše**.
   - Pokud jste vybrali **Tabulku** v kroku 6, vyberte konkrétní **Číslo dodavatele** pro profil účtování v poli **Vztah k účtu**.
   - Pokud jste vybrali **Skupinu** v kroku 6, vyberte konkrétní **Skupinu dodavatele** pro profil účtování v poli **Vztah k účtu**.
   - Pokud jste vybrali **Vše** v kroku 6, pole **Vztah účtu** zůstane prázdné.

8. Chcete-li spojit určitou skupinu DPH s vybraným typem zaúčtování, vyberte **Skupinu DPH**. Pokud toto pole ponecháte prázdné, bude se typ zaúčtování vztahovat ke všem existujícím daňovým skupinám. Účtování stanovené pro daňové skupiny se vztahuje pouze k transakcím, které se provádí v souvislosti s prodeji a nákupy.

9. V poli **Hlavní účet** zadejte číslo účtu, na který chcete zaúčtovat typ účtu. Vyberte jedno z existujících čísel účtu v tabulce účtů.
