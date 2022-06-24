---
title: Účetní profily zásob
description: Tento článek poskytuje přehled účetních profilů zásob.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901335"
---
# <a name="inventory-posting-profiles"></a>Účetní profily zásob

[!include [banner](../includes/banner.md)]

Účetní profily zásob řídí zaúčtování transakcí zásob dílčí z hlavní knihy do hlavní knihy Transakce dílčí knihy zásob lze generovat z mnoha modulů, včetně **Prodej a marketing**, **Zásobování a zdroje**, **Řízení výroby** a dalších. Transakce dílčí knihy zásob mohou být zaúčtovány kdykoli je položka použita v prodejní objednávce nebo nákupní objednávce. 

Další transakce dílčí knihy zásob mohou být zaúčtovány:
- Při každé aktualizaci dokladu.
- Když je zaúčtován dodací list prodejní objednávky nebo faktura.
- Když se vygeneruje příjemka produktu nákupní objednávky nebo faktura.

Další informace viz téma Transakce dílčí knihy zásob.

## <a name="inventory-transaction-overview"></a>Přehled transakcí zásob

Každá transakce dílčí knihy zásob obsahuje:
 - Množství 
 - Cena 
 - Web 
 - Sklad 
 - Umístění 

Transakce dílčí knihy zásob vytvářejí dvě entity v hlavní knize prostřednictvím fyzického účtování a finančního účtování. Více informací najdete v tématu [Fyzické a finanční aktualizace](/supply-chain/cost-management/physical-financial-updates.md).
Následující příklad je nákupní objednávka se třemi řádky. V tomto příkladu předpokládejme, že celá objednávka je určena pro jedno místo a sklad. Každý řádek nákupní objednávky má jeden související záznam InventTrans – známý také jako transakce zásob – a každý řádek obsahuje množství 10. Následující diagram ukazuje vztah jednoho záhlaví nákupní objednávky ke třem řádkům nákupní objednávky, každý s jedním záznamem InventTrans.

![Diagram vztahů pro nákupní objednávku se třemi řádky, každý s jedním záznamem InventTrans.](./media/InventTransRelationship.PNG)

Množství 5 je přijato na prvním řádku nákupní objednávky. Celé množství pro druhý řádek a žádné přijaté množství na třetím řádku nákupní objednávky. Nyní existuje druhá transakce zásob související s prvním řádkem nákupní objednávky. Transakce pro druhý řádek nákupní objednávky bude aktualizována na stav **Přijato** a třetí transakce zůstane stejná. Následující diagram ukazuje vztah s dalším záznamem InventTrans pro řádek nákupní objednávky 1.

![Diagram vztahů pro nákupní objednávku se třemi řádky. Jeden řádek je částečně přijat a zobrazuje dva záznamy InventTrans.](./media/InventTransRelationshipPartialReceipt.PNG)

V tomto příkladu bude doklad zaúčtován do hlavní knihy; toto je fyzický doklad. Skupina modelů položek je konfigurována pro zaúčtování fyzické zásoby a všechny položky používají stejnou skupinu modelů položek. Profil účtování zásob používá jedinou sadu hlavních účtů. Bude vytvořen jeden doklad a záznam InventTrans propojí oba záznamy InventTrans 1 a InventTrans 2 se stejným dokladem.

Dále je přijata faktura za množství, které bylo přijato na řádcích 1 a 2. V hlavní knize se vytvoří další doklad; toto je finanční doklad. Skupina modelů položek je konfigurována pro zaúčtování finančních zásob. Nový druhý doklad souvisí se záznamy InventTrans 1 a InventTrans 2.

V závislosti na kalkulačním modelu může existovat třetí účtování hlavní knihy pro vaše transakce dílčí knihy zásob související s uzavřením a vypořádáním zásob. Další informace naleznete v tématu [Uzávěrka zásob](/supply-chain/cost-management/inventory-close.md). Podrobnosti o všech transakcích zásob můžete zobrazit na stránce **Řízení zásob** > **Dotazy a sestavy** > **Transakce**.

>[!Important]
> Transakce zásob budou rozděleny pro každou jedinečnou kombinaci dimenzí zásob a pro každou dílčí aktualizaci. To bylo ukázáno v předchozím příkladu pro dílčí aktualizace.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Rozdělení zásob na základě příkladu dimenze zásob

Řádek nákupní objednávky 3 v příkladu je serializovaná položka. Během procesu příjmu je pro objednávku zaregistrováno deset sériových čísel. Transakce zásob bude rozdělena do 10 transakcí zásob. Následující diagram ukazuje vztah a další transakce zásob, každá s vlastním sériovým číslem souvisejícím s řádkem 3 nákupní objednávky.

![Diagram vztahů pro nákupní objednávku se třemi řádky. Jeden řádek je serializován a zobrazuje další záznamy InventTrans](./media/InventTransRelationshipSerialNumber.PNG)

Ve výše uvedeném příkladu bude vytvořen jeden další doklad, pokud je každé sériové číslo přijato na jedné příjemce produktu. Pole fyzického dokladu bude spojeno s každým sériovým číslem. Totéž platí pro finanční aktualizaci, když fakturujete nákupní objednávku.

## <a name="inventory-transactions"></a>Skladové transakce

Transakce zásob můžete zobrazit na stránce **Transakce zásob** v části **Řízení zásob a skladů** nebo **Správa nákladů**. Můžete také zobrazit transakce zásob související s určitým řádkem zdrojového dokladu – jako je řádek nákupní objednávky nebo řádek prodejní objednávky – výběrem položky **Zásoby** a poté výběrem možnosti **Transakce**. 

Stránka **Transakce zásob** obsahuje následující pole.

| Pole            | Popis                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Číslo položky      | Číslo řádku související s transakcí.                                                                  |
| Fyzické datum    | Datum, kdy zásoby dorazí na sklad, opustí sklad, spotřebují se ve výrobě nebo se vyrobí. Například datum zaúčtování
zaúčtování dodacího listu u prodejní objednávky nebo účtování příjmu produktu u nákupní objednávky.                             |
| Finanční datum   | Datum uzavření transakce zásob a zaznamenání nákladů v hlavní knize. Například datum zaúčtování pro fakturu 
generování pro nákupní nebo prodejní objednávku. Po vyplnění finančního data nejsou aktualizace referenčního dokladu povoleny. |
| Reference        | Označuje zdroj transakce a typ dokladu, který je zobrazen v poli **Číslo**. Například prodejní objednávka, nákupní objednávka nebo příjemka převodního příkazu.                                                 |
| Číslo           | Označuje referenční ID pro transakci. Například, pokud pole **Reference** ukazuje na prodejní objednávku, pole **Číslo** obsahuje číslo prodejní objednávky.                                                       |
| Příjem (stav) | U transakcí zásob, které jsou příjmy, toto pole udává stav příjemky. Například nákupní objednávka je příjemka a její stav může být **Objednáno** nebo **Zakoupeno**.                                                            |
| Výdej (stav)   | U transakcí zásob, které jsou výdaje, toto pole udává stav výdeje. Například prodejní objednávka je výdej a stav může být **Na objednávce** nebo **Prodáno**.                         |
| Množství         | Množství transakce zásob. Kladná čísla se používají pro příjemky do zásob, zatímco záporná čísla se používají pro výdejky ze zásob.                                                                                                                          |
| Jednotka             | Měrná jednotka, ve které je množství vyjádřeno.                                                                                   |
| Množství v SH      | Množství skutečné hmotnosti pro transakci. Další informace naleznete v [O položkách skutečné hmotnosti](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Jednotka SH          | Jednotka skutečné hmotnosti, ve které je vyjádřeno množství skutečné hmotnosti.                                                         |
| Částka nákladů      | Konečné náklady transakce zásob. Toto pole se vyplní, když je transakce finančně aktualizována. V závislosti na metodice kalkulace může proces uzavření zásob a úprav toto pole aktualizovat.                            |

## <a name="inventory-status"></a>Stav skladu

Každá transakce zásob má stav, který je zobrazen buď v poli **Příjem**, nebo poli **Výdej**. Pole, které se použije, závisí na typu transakcí zásob. Příjmy jsou transakce, které zvyšují zásoby. Například nákupní objednávka s kladným množstvím nebo vratka prodejní objednávky se záporným množstvím. Výdeje jsou transakce zásob, které snížily zásoby. Například prodejní objednávka s kladným množstvím nebo vratka nákupní objednávky se záporným množstvím.

### <a name="receipt-status"></a>Stav příjmu

Následující tabulka popisuje stav **Příjmu**.

| **Stav příjmu** | **popis**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Objednáno            | Počáteční stav jakékoli transakce zásob, která představuje příjem. To zahrnuje nákupní objednávky s kladným množstvím, výrobní zakázky nebo vratky prodejní objednávky se záporným množstvím.                                                   |
| Registrováno         | Tento stav se používá, když probíhá proces příjmu ve dvou krocích nebo když se příchod položky používá k označení, že produkt dorazil. Používá se, když jsou k objednávce „přidělována“ nebo registrována čísla šarží nebo sériová čísla. Další informace o doručení položky naleznete v tématu [Přehled doručení](/supply-chain/inventory/arrival-overview.md). |
| Přijato           | Tento stav se používá, když je transakce fyzicky aktualizována. U nákupní objednávky je to okamžik, kdy je zaúčtována příjemka produktu. U vratky prodejní objednávky je to okamžik, kdy je zaúčtován dodací list.                                                                            |
| Koupeno          | Tento stav se používá, když je transakce finančně aktualizována. U nákupní objednávky nebo vratky prodejní objednávky je to okamžik, kdy je vygenerována faktura.                                                                                             |

### <a name="issue-status"></a>Stav výdeje

Následující tabulka popisuje stav **Výdeje**.

| **Stav výdeje**  | **popis**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Na objednávce          | Počáteční stav jakékoli transakce zásob, která představuje výdej. To zahrnuje prodejní objednávky s kladným množstvím, řádky kusovníku nebo receptury výrobní zakázky nebo vratky nákupní objednávky se záporným množstvím.                                             |
| Rezervované – objedn.  | Tento stav zásob označuje, že zásoby jsou rezervovány pro objednávku, která byla vytvořena, ale ještě nebyla fyzicky přijata do zásoby. Po přijetí zásob se stav automaticky aktualizuje na **Rezervované – fyzicky**. Více informací o rezervacích najdete v tématu [Rezervace skladových množství](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Rezervované – fyzicky | Tento stav označuje, že zásoby byly přidělen nebo rezervovány pro konkrétní objednávku. Když jsou zásoby rezervovány, nejsou fyzicky dostupné pro jiné objednávky.                                 |
| Vyzvednuto         | To znamená, že zásoby byly vyskladněny ze skladu. Zásoby jsou stále fyzicky ve skladu, nebyly odebrány, ale nejsou k dispozici pro jiné objednávky.  |
| Odečteno          | Tento stav se používá, když je transakce fyzicky aktualizována. U prodejní objednávky se jedná o zaúčtování dodacího listu; u vratky nákupní objednávky při zaúčtování příjemky produktu.                                                                      |
| Prodáno              | Tento stav se používá, když je transakce finančně aktualizována. U nákupní objednávky nebo prodejní objednávky je to okamžik, kdy je vygenerována faktura.|

Další informace o transakcích zásob naleznete v tématu [Detaily transakcí zásob](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Konfigurujte profil zaúčtování zásob

Chcete-li konfigurovat profil zaúčtování zásob, postupujte následujícím způsobem:

1.  Otevřete **Řízení zásob** > **Nastavení** > **Zaúčtování** > **Zaúčtování**.
2.  Vyberte kartu pro typ transakce. Například vyberte **Nákupní objednávka**.
3.  Vyberte přepínač pro typ účtování. Například vyberte **Nákupní výdaje**.
4.  Zvolte **Nové**.
5.  V poli **Kód položky** vyberte **Tabulku**, **Skupinu**, **Vše** nebo **Kategorii**. Chcete-li například konfigurovat profil účtování pro určitou skupinu položek, vyberte **Skupina**.
     - Pokud jste vybrali **Tabulku** v kroku 5, vyberte konkrétní Číslo položky pro profil účtování v poli **Vztah položky**.
     - Pokud jste vybrali **Skupinu** v kroku 5, vyberte konkrétní **Skupinu položky** pro profil účtování v poli **Vztah položky**.
     - Pokud jste vybrali **Vše** v kroku 5, pole **Vztah položky** zůstane prázdné.
     - Pokud jste vybrali **Kategorii** v kroku 5, pole **Vztah položky** zůstane prázdné. Použijte pole **Vztah kategorií** a vyberte kategorii, pro kterou účetní profil platí.

6.  V poli **Kód účtu** vyberte možnost pro **Tabulku**, **Skupinu** nebo **Vše**. Chcete-li například profil účtování použít pro všechny dodavatele, vyberte **Vše**.
     - Pokud jste vybrali **Tabulku** v kroku 5, vyberte konkrétní číslo dodavatele pro profil účtování v poli **Odkaz na účet**.
     - Pokud jste vybrali **Skupinu** v kroku 5, vyberte konkrétní skupinu dodavatele pro profil účtování v poli **Odkaz na účet**.
     - Pokud jste vybrali **Vše** v kroku 5, pole **Odkaz na účet** zůstane prázdné.

7.  Chcete-li spojit určitou skupinu DPH s vybraným typem zaúčtování, vyberte **Skupinu DPH**. Pokud je toto pole prázdné, bude se typ zaúčtování vztahovat ke všem existujícím daňovým skupinám. Účtování určené pro daňové skupiny se vztahuje pouze na transakce prodeje a nákupu.
8.  V poli **Hlavní účet** zadejte číslo účtu, na který chcete zaúčtovat typ účtu. Pokud ještě není vytvořeno číslo účtu, které se má použít pro typ účetnictví, můžete vytvořit nový účet. Nový účet vytvoříte na stránce **Podrobnosti o hlavním účtu** v hlavní knize.

## <a name="additional-resources"></a>Další prostředky

Každá karta na stránce **Profil účtování zásob** se týká dílčí knihy v Dynamics 365 Supply Chain Management. Další informace naleznete zde:
-   [Zaúčtování prodejní objednávky](sales-order-posting.md)
-   [Zaúčtování nákupní objednávky](purchase-order-posting.md)
-   [Zaúčtování zásob](inventory-posting.md)
-   [Účtování řízení výroby](production-posting.md)
-   [Účtování standardní odchylky nákladů](standard-cost-variance-posting.md)
