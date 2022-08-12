---
title: Zaúčtování nákupní objednávky
description: Tento článek obsahuje informace o kartě Nákupní objednávka na stránce Profily zaúčtování zásob.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151025"
---
# <a name="purchase-order-posting"></a>Zaúčtování nákupní objednávky

Karta **Nákupní objednávka** na stránce **Profily zaúčtování zásob** se používá ke kontrole toho, jak se nákupní objednávky zaúčtují do hlavní knihy. Do hlavní knihy pro nákupní objednávku jsou zaúčtovány dvě hlavní činnosti: 

- Příjemka produktu
- Faktura

Pro zaúčtování fyzické transakce (příjemka produktu) do hlavní knihy pro nákupní objednávku musejí být zapnuta následující zaškrtávací políčka:

- Na stránce **Parametry řízení zásob a skladu** musí být zaškrtnuto políčko **Zaúčtovat příjemku produktu do hlavní knihy**.
- Zaškrtávací políčka **Zaúčtovat fyzické zásoby** a **Časově rozlišit pasiva na příjemce produktu** na stránce **Skupiny modelů položek**.

Hlavní účet musí být uvedený na stránce **Profil účtování zásob** pro následující typy zaúčtování:

- Náklady na nákup přijatého materiálu
- Nákupní výdaj, bez faktury
- Nákup, časové rozlišení

Pro zaúčtování finanční transakce (faktura) do hlavní knihy pro nákupní objednávku musí být splněny následující podmínky:

- Na stránce **Skupiny modelů položek** musí být pro položku vybranou na řádku nákupní objednávky zaškrtnuto políčko **Zaúčtovat finanční zásoby**.
- Hlavní účet musí být uvedený na stránce **Profil účtování zásob** pro následující typy zaúčtování:
  - Fakturované náklady na nákup materiálu
  - Nákupní výdaj pro produkt
  - Nákupní výdaje
  - Sleva (volitelná)

## <a name="fixed-receipt-price-posting"></a>Zaúčtování pevné ceny příjmu

Jako alternativu k výběru možnosti **Standardní cena** v poli **Model zásob** na stránce **Skupiny modelů položek** můžete jako standardní cenu produktu použít pevnou cenu příjemky. Hlavním rozdílem je při použití **Pevné ceny příjmu** to, že při zaúčtování příjemky do zásob se pro položku použije aktuální nákladová cena. Pro **Pevnou cenu příjmu** neexistuje žádný proces přecenění nákladů; při zaúčtování finanční aktualizace se použije aktuální nákladová cena v době zaúčtování. Pokud se nákladová cena použitá při příjmu liší od ceny na faktuře, bude odchylka zaúčtována na účty zisků a ztrát s pevnou cenou příjmu.

Chcete-li pro produkt použít pevnou cenu příjmu, musíte konfigurovat následující údaje:

- Na stránce **Skupiny modelů položek** zapněte zaškrtávací políčka **Zaúčtovat fyzické zásoby** a **Pevná cena příjmu**. 
- Na stránce **Parametry řízení zásob a skladu** zaškrtněte políčko **Zaúčtovat dodací list do účetní knihy**.
- Na stránce **Profil účtování zásob** zadejte hlavní účty pro následující typy účtování:
  - Zisk pevné ceny příjmu
  - Ztráta pevné ceny příjmu
  - Protiúčet pevné ceny příjmu

Další informace naleznete v tématu [Pevná cena příjmu](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Zaúčtování doprovodných nákupních nákladů a skladových odchylek

Pokud plánujete účtovat nákupní poplatky a skladové odchylky, postupujte takto:

- Na stránce **Parametry závazků** vyberte na kartě **Faktura** zaškrtávací políčko **Zaúčtovat na účet poplatků v hlavní knize**.
- Na stránce **Skupiny modelů položek** u položky vybrané na řádku nákupní objednávky zapněte políčka **Zaúčtovat fyzické zásoby**, **Zaúčtovat finanční zásoby** a **Časově rozlišit pasiva na příjemce produktu**.
- Na stránce **Parametry modulu Zásobování a zdroje** zapněte zaškrtávací políčko **Generovat poplatky v příjemce produktu**.
- Na stránce **Parametry řízení zásob a skladu** zaškrtněte políčko **Zaúčtovat dodací list do účetní knihy**.

Na stránce **Profil účtování zásob** musíte uvést hlavní účty pro následující typy zaúčtování:

- Nákupní výdaj, bez faktury
- Nákupní výdaj pro produkt
- Skladová odchylka

> [!NOTE]
> Typ zaúčtování **Náklady** se nepoužívá, když je vybrán parametr **Zaúčtovat na účet poplatků v hlavní knize**.

Další informace najdete v tématu [Princip účtování na účet poplatků](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Ukázka konfigurace profilu zveřejňování

Následující tabulka ukazuje příklady výchozích typů účtování s ukázkovými hlavními účty a popisy:

- Sloupec **Clearingový účet** označuje, že typ účtování je clearingový účet. Částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce. 
- Sloupec **P/F** označuje **P** pro fyzické zaúčtování a **F** pro finanční zaúčtování. 
- Sloupec **Sledovat** udává, zda je hlavní účet pro určitý typ účtování obvykle stejný jako jiný typ účtování. Hodnota ve sloupci označuje typ účtování, který se obvykle používá.

> [!NOTE]
> Hlavní účty a názvy hlavních účtů jsou pouze návrhy. Doporučujeme<!--note from editor: Via Writing Style Guide.--> , abyste ve spolupráci se svým účetním určili nejlepší konfiguraci pro vaše obchodní potřeby.


| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Má dáti/Dal? | Clearingový účet | P/F | Sledovat | Popis |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Náklady na nákup přijatého materiálu | 140100</br>140101 | Zásoby materiálů</br>Expedované nefakturované materiály | Materiál | Debet | Ano | P | Fakturované náklady na nákup materiálu | Používá se, když je zaúčtován příjem produktu nákupní objednávky, kompenzace na účet je Nákupní výdaje, nevyfakturované. Částka na tomto účtu je stornována při zaúčtování faktury nákupní objednávky. |
| Nákupní výdaj, bez faktury | 600180 | Příjemky materiálů | Výdaje | Debet | Ano | P | |Používá se, když je zaúčtována příjemka produktu nákupní objednávky. Pro příjem jsou vytvořeny dva doklady pro sledování odchylek nákupní ceny při použití standardních nákladů. Protiúčtem k účtu na prvním dokladu je Časové rozlišení nákupu. Protiúčtem k účtu na druhém dokladu je součet účtů Náklady na nákup přijatého materiálu a Odchylka nákupní ceny. Částky na zaúčtované na tomto účtu jsou stornovány při zaúčtování faktury nákupní objednávky. |
| Fakturované náklady na nákup materiálu | 140100 | Zásoby materiálů | Materiál | Debet | Číslo | F  |Náklady na nákup přijatého materiálu | Používá se, když je zaúčtována faktura nákupní objednávky. Protiúčtem k tomuto účtu je Nákupní výdaj pro produkt. Tento účet představuje zásoby ve vaší rozvaze. Použitý účet je obvykle stejný účet, který se používá pro náklady na dodané jednotky a náklady na fakturované jednotky u prodejní objednávky. |
| Nákupní výdaj pro produkt | 600180 | Příjemka materiálu | Výdaje | Kredit | Ano | F  | |Používá se, když je zaúčtována faktura nákupní objednávky. Pro fakturu jsou vytvořeny dva doklady pro sledování odchylek nákupní ceny při použití standardních nákladů. Zápočet na tento účet je nákupní výdaj, nevyfakturovaný účet, který se používá při účtování příjemky a stornuje se při účtování faktury. Představuje náklady na zásoby nakoupené při fakturaci, které nejsou zohledněny na účtu zásob v rozvaze. Jedná se o účtování zisků a ztrát pro rozptyl nákupní ceny, který se nejčastěji vyskytuje u nákupů standardních nákladových položek.|
| Zisk pevné ceny příjmu (Nákup, zisk pevné ceny příjmu*) | 510310 | Odchylka nákupní ceny | Výdaje | Kredit | Číslo | F | Ztráta pevné ceny příjmu | Používá se, když je zaúčtována faktura nákupní objednávky a existuje rozdíl mezi fakturovanou cenou a výchozí cenou položky. Tento účet se používá, když je rozdíl vyšší. Protiúčtem je Protiúčet pevné ceny příjmu. |
| Ztráta pevné ceny příjmu (Nákup, ztráta pevné ceny příjmu*) | 510310 | Odchylka nákupní ceny | Výdaje | Debet | Číslo | F | Zisk pevné ceny příjmu | Používá se, když je zaúčtována faktura nákupní objednávky a existuje rozdíl mezi fakturovanou cenou a výchozí cenou položky. Tento účet se používá, když je rozdíl nižší. Protiúčtem je Protiúčet pevné ceny příjmu. |
| Protiúčet pevné ceny příjmu (Nákup, protiúčet pevné ceny příjmu*) | 140900 | Skladová odchylka | Materiál | Oboje | Číslo | F  | |Používá se, když je zaúčtována faktura nákupní objednávky a existuje rozdíl mezi fakturovanou cenou a výchozí cenou položky. Tento účet je protiúčtem účtů Zisk pevné ceny příjmu a Ztráta pevné ceny příjmu. |
| Náklady | Není k dispozici | Není k dispozici | Není k dispozici | Není k dispozici | Není k dispozici | Není k dispozici | Není k dispozici | Tento účet se již nepoužívá. Místo toho použijte Skladovou odchylku. |
| Skladová odchylka | 600170 | Skladová odchylka | Výdaje | Kredit | Číslo | Oboje | | Tento účet se používá, když: <ul><li>Mezi příjemkou produktu a fakturou je rozdíl v jednotkové ceně.</li><li>K položce jsou účtovány poplatky (náklady).</li><li>K zakoupeným položkám byly<!--note from editor: Edit okay?--> přidány nepřímé náklady. </li><li>Protiúčtem tohoto účtu je Nákupní výdaj, bez faktury.</li></ul> |
| Nákup, časové rozlišení | 200140 | Časově rozlišené nákupy | Pasiva | Kredit | Y | P | |Používá se, když je zaúčtována příjemka produktu nákupní objednávky a je povolena možnost časového rozlišení částek nákupu. |
| Časově rozlišená DPH při příjmu | 250500 | Časově rozlišená DPH | Pasiva | Kredit | Y | Oboje  | |Tento účet se použije, když vyberete možnost **Zaúčtovat fyzickou DPH** na stránce **Parametry modulu Řízení zásob a skladu** a máte nákupní objednávku s DPH. Částka se zaúčtuje, když objednávku fyzicky aktualizujete (příjem produktu), a stornuje se, když objednávku zaúčtujete finančně (faktura). |
| Příjem dlouhodobého majetku (debet dlouhodobého majetku*) | 180100 | Hmotný dlouhodobý majetek | Materiál | Debet | N | Oboje | Oboje | Tento účet se používá, když vyberete možnost Dlouhodobý majetek na řádku nákupní objednávky. Integrace nákupní objednávky byla konfigurována tak, aby pořizovala dlouhodobý majetek na základě příjmu produktu nebo faktury. Další informace o integraci nákupní objednávky dlouhodobého majetku naleznete v tématu [Pořízení majetku pomocí zásobování](/fixed-assets/acquire-assets-procurement). |
| Nákupní výdaje | 618900 | Vedlejší výdaje | Výdaje | Debet | N | Oboje | |Používá se při zaúčtování příjemky produktu nebo faktury pro nákupní objednávku, kde položky nejsou na skladě, nebo se používá kategorie zásobování. |
| Záloha | 132190 | Předplacený výdaj | Materiál | Debet | N | Oboje | | Používá se při zpracování zálohové faktury na nákupní objednávce. |


\*Hodnoty uvedené v závorkách představují hodnotu, která je použita v poli **Typ zaúčtování** na stránce **Transakce dokladu**. Můžete zobrazit **Typ účtování** na stránce **Transakce dokladů** na kartě **Všeobecné**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Účtování dlouhodobého majetku s nákupními objednávkami

Pokud použijete modul **Dlouhodobý majetek** a plánujete nákup dlouhodobého majetku prostřednictvím nákupních objednávek, musíte konfigurovat typ účtování **Příjem dlouhodobého majetku** na kartě **Nákupní objednávka** stránky **Profil účtování zásob**. Více informací najdete v tématech [Integrace dlouhodobého majetku](/fixed-assets/fixed-asset-integration.md) a [Vytvoření a získání majetku z modulu Závazky](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Zaúčtování zálohové faktury nákupní objednávky

Pokud plánujete používat funkci **Zálohová faktura** u nákupních objednávek, musí být na kartě **Nákupní objednávka** na stránce **Profil účtování zásob** vybrán typ účtování **Záloha**. Více informací najdete v tématu [Zálohové faktury vs. zálohové platby](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Zaúčtování nákupní žádanky a potvrzení nákupní objednávky

Nákupní žádanky a potvrzení nákupních objednávek lze také konfigurovat tak, aby do hlavní knihy zaúčtovaly předběžná břemena a břemena. Tato účtování jsou řízena definicí účtování. Další informace naleznete v tématu [O břemenech nákupní objednávky](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Zaúčtování kategorie zásobování

Jako alternativu k nastavení účtování zásob pro všechny položky, skupinu položek nebo jednu položku můžete nastavit kategorie a řídit účtování v hlavní knize podle kategorií zásobování. Další informace o nastavení kategorií a jejich přiřazení k produktům naleznete v části [Ukázka konfigurace profilu zveřejňování](#sample-posting-profile-configuration) dříve v tomto článku.

Při použití kategorií s nákupními objednávkami nebo fakturami dodavatele je třeba hierarchii kategorií přiřadit k typu **Hierarchie kategorií zásobování** na stránce **Přiřazení role hierarchie kategorií**.

### <a name="vendor-invoices-with-procurement-categories"></a>Faktury dodavatele s kategoriemi zásobování

Pokud vaše organizace používá nákupní objednávky pro některé nákupy a pro jiné ne, můžete zpracovat faktury nesouvisející s nákupní objednávkou různými způsoby. To zahrnuje používání deníků na stránce **Závazky** nebo **Nevyřízené faktury dodavatele**, která se používá ke generování faktur za nákupní objednávky. Při vytváření faktur nesouvisejících s nákupní objednávkou budete muset vytvořit kategorie nákupu pro každý typ výdajů. Budete muset namapovat kategorii na správný účet výdajů na stránce **Profily zaúčtování zásob**.

Přesný počet kategorií se bude lišit v závislosti na počtu výdajových účtů, které používáte k zaúčtování faktur. Budete potřebovat alespoň jednu kategorii zásobování pro každý hlavní účet, na který účtujete faktury za nenákupní objednávky. Pro jeden hlavní účet lze použít mnoho kategorií. To může být užitečné pro použitelnost, vyhledávání a vykazování typů výdajů, které používáte.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Výhody použití kategorií zásobování u faktur dodavatelů

Mezi výhody použití kategorií zásobování u faktur dodavatelů patří:

- Konzistentní uživatelské prostředí: Když nakonfigurujete kategorie zásobování u všech výdajů, které nesouvisejí s nákupními objednávkami, uživatelům stačí jedno školení procesu fakturace na stránce **Nevyřízené faktury dodavatele**.
- Vylepšené prostředí pro vytváření sestav: Když nakonfigurujete kategorie zásobování pro všechny položky a všechny výdaje, které nesouvisejí s nákupní objednávkou, sestava výdajů na nákup bude analyzovat výdaje podle dodavatele, kategorie a dalších.
- Konzistentní pracovní postup: Když používáte **Nevyřízené faktury dodavatele** ke zpracování všech faktur, můžete vytvořit konzistentní pracovní postup a schvalovací proces s využitím jediného pracovního postupu.

## <a name="consignment-inventory-posting"></a>Zaúčtování zásob dodávky

Zásoby dodávky používají stejné účtování jako ostatní zakoupené položky. Klíčový rozdíl je v tom, že při příjmu zásob nejsou zaznamenány žádné transakce hlavní knihy. Aby šlo převést vlastnictví na organizaci, když je zaúčtován deník **Změna vlastnictví zásob**, je vygenerován doklad k zaznamenání nákladů na položku. Další informace naleznete v tématu [Nastavení zásilky](/supply-chain/inventory/consignment.md).
