---
title: Začínáme s výpočtem daně
description: Tento článek vysvětluje, jak nastavit výpočet daně.
author: EricWangChen
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.custom: intro-internal
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: 2b9af7a8bef9d479c4f2ec59ef533403a74251b1
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573298"
---
# <a name="get-started-with-tax-calculation"></a>Začínáme s výpočtem daně

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace o tom, jak začít pracovat s výpočtem daně. Části v tomto článku vás provedou návrhem na vysoké úrovni a kroky konfigurace ve službách Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance a Dynamics 365 Supply Chain Management. 

Nastavení se skládá ze tří hlavních kroků.

1. V LCS nainstalujte doplněk pro výpočet daně.
2. V RCS nastavte funkci výpočtu daně. Toto nastavení není specifické pro určitou právnickou osobu. Lze jej sdílet mezi právnickými osobami v aplikacích Finance a Supply Chain Management.
3. Ve Finance a Supply Chain Management nastavte parametry výpočtu daně podle právnické osoby.

## <a name="high-level-design"></a>Návrh na vysoké úrovni

### <a name="runtime-design"></a><a name="runtime"></a> Návrh runtime

Následující obrázek znázorňuje návrh runtime na vysoké úrovni Tax Calculation. Protože Tax Calculation lze integrovat s více aplikacemi Dynamics 365, na obrázku je jako příklad použita integrace s Finance.

1. Transakce, jako je prodejní objednávka nebo nákupní objednávka, se vytvoří ve Finance.
2. Finance automaticky použije výchozí hodnoty skupiny DPH a skupiny DPH zboží.
3. Když je v transakci zvoleno tlačítko **DPH**, spustí se výpočet daně. Finance poté odešle datovou část do služby Tax Calculation.
4. Služba Tax Calculation porovnává datovou část s předdefinovanými pravidly ve funkci daně, aby bylo možné najít přesnější skupinu DPH a skupinu DPH zboží současně.

    - Pokud lze datovou část porovnat s maticí **Použitelnost daňové skupiny**, přepíše hodnotu skupiny DPH odpovídající hodnotou daňové skupiny v pravidle použitelnosti. V opačném případě bude nadále používat hodnotu skupiny DPH z Finance.
    - Pokud lze datovou část porovnat s maticí **Použitelnost daňové skupiny zboží**, přepíše hodnotu skupiny DPH zboží odpovídající hodnotou daňové skupiny zboží v pravidle použitelnosti. V opačném případě bude nadále používat hodnotu skupiny DPH zboží z Finance.

5. Služba Tax Calculation určí konečný daňový kód průnikem skupiny DPH a skupiny DPH zboží.
6. Služba Tax Calculation vypočítá daň na základě konečných daňových kódů, které určila.
7. Služba Tax Calculation vrátí výsledek výpočtu daně do Finance.

![Návrh runtime Tax Calculation.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Konfigurace na vysoké úrovni

Následující kroky poskytují základní přehled procesu konfigurace pro službu Tax Calculation.

1. V LCS nainstalujte doplněk **Tax Calculation** do projektu LCS.
2. V RCS vytvořte funkci **Tax Calculation**.
3. V RCS nastavte funkci **Tax Calculation**:

    1. Vyberte verzi daňové konfigurace.
    2. Vytvořte daňové kódy.
    3. Vytvořte daňovou skupinu.
    4. Vytvořte daňovou skupinu zboží.
    5. Volitelné: Vytvořte použitelnost daňové skupiny, pokud chcete přepsat výchozí skupinu DPH, která je zadána z hlavních dat zákazníka nebo dodavatele.
    6. Volitelné: Vytvořte použitelnost skupiny zboží, pokud chcete přepsat výchozí skupinu DPH zboží, která je zadána z hlavních dat zboží.

4. V RCS dokončete a publikujte funkci **Tax Calculation**.
5. Ve Finance vyberte zveřejněnou funkci **Tax Calculation**.

Po provedení těchto kroků se následující nastavení automaticky synchronizují z RCS do Finance.

- Kódy DPH
- Skupiny DPH
- Skupiny DPH položky

Zbývající části tohoto článku poskytují podrobnější informace krocích konfigurace.

## <a name="prerequisites"></a>Předpoklady

Než budete moci provést zbývající postupy uvedené v tomto článku, musí být splněny následující předpoklady:<!--TO HERE-->

- Musíte mít přístup ke svému účtu LCS a nasadit projekt LCS s prostředím úrovně 2 (nebo vyšším), ve kterém běží Dynamics 365 verze 10.0.21 nebo novější.
- Pro svou organizaci musíte vytvořit prostředí RCS a musíte mít přístup ke svému účtu. Další informace o tom, jak vytvořit prostředí RCS, najdete v tématu [Přehled Regulatory Configuration Service](rcs-overview.md).
- Následující funkce musí být zapnuty v pracovním prostoru **Správa funkcí** vašeho nasazeného prostředí Finance nebo Supply Chain Management, na základě vašich obchodních potřeb:

    - Služba výpočtu daně
    - Podporovat více DIČ
    - Daň v převodním příkazu

- Následující funkce musí být zapnuty v pracovním prostoru **Správa funkcí** vašeho nasazeného prostředí RCS.

    - Globalizační funkce

- Následující role by měly být podle potřeby přiřazeny uživatelům ve vašem prostředí RCS:

    - Návrhář elektronického výkaznictví
    - Vývojář globalizační funkce
    - Vývojář daňového modulu
    - Konzultant funkcí daňového modulu
    - Vývojář daňových služeb

## <a name="set-up-tax-calculation-in-lcs"></a>Nastavení výpočtu daně v LCS

1. Přihlaste se do [LCS](https://lcs.dynamics.com)
2. Dokončete nastavení integrace Microsoft Power Platform. Další informace naleznete v tématu [Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Vyberte jedno ze svých nasazených prostředí a pak vyberte možnost **Nainstalovat nový doplněk**.
4. Vyberte možnost **Výpočet daně**.
5. Přečtěte si smluvní podmínky, vyjádřete s nimi souhlas a poté vyberte možnost **Instalovat**.

## <a name="set-up-tax-calculation-in-rcs"></a>Nastavení výpočtu daně v RCS

Kroky v této části nesouvisí s konkrétním právním subjektem. Tento postup musíte dokončit pouze jednou a můžete jej dokončit u jakékoli právnické osoby v RCS.

1. Přihlaste se do [RCS](https://marketing.configure.global.dynamics.com/).
2. V pracovním prostoru **Elektronické výkaznictví** přidejte nového poskytovatele konfigurace. Jako název poskytovatele použijte název vaší společnosti. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Vyberte poskytovatele konfigurace, kterého jste právě vytvořili, a pak vyberte možnost **Nastavit jako aktivní**.
4. Vyberte poskytovatele konfigurace **Microsoft** a poté vyberte **Úložiště**.
5. V poli **Typ** vyberte **Globální**.
6. Zvolte **Otevřít**.
7. Přejděte do části **Model daňových dat**, rozbalte strom souborů a poté vyberte možnost **Konfigurace daní**.
8. Vyberte správnou [verzi konfigurace daně](global-tax-calcuation-service-overview.md#versions) na základě vaší verze Finance a poté vyberte **Import**.
9. V pracovním prostoru **Funkce globalizace**, vyberte **Funkce**, vyberte dlaždici **Výpočet daně** a poté vyberte příkaz **Přidat**.
10. Vyberte jeden z následujících typů funkce:

    - **Nová funkce** – Vytvořte nastavení funkce, která má prázdný obsah.
    - **Na základě stávající funkce** – Vytvořte funkci z existující funkce a zkopírujte obsah z nastavení existující funkce.

11. Zadejte název a popis nové funkce a poté vyberte **Vytvořit funkci**.

    Po vytvoření funkce se automaticky vytvoří její koncept. Můžete vybrat **Získejte tuto verzi**, chcete-li přeskládat rámcovou verzi na libovolné dokončené verzi.

12. Vyberte konceptovou verzi funkce a poté vyberte příkaz **Upravit**. Stránka **Nastavení výpočtu daně** je vyplněna.
13. Vyberte **Verze konfigurace**. Měla by se zobrazit verze konfigurace, kterou jste importovali v kroku 8.

    Společnost Microsoft poskytuje výchozí konfiguraci daně pro výpočet daně. Tato konfigurace pokrývá většinu požadavků na chování výpočtu daně. Bude aktualizován na základě zpětných vazeb trhu. Pokud musíte rozšířit konfiguraci, aby splňovala konkrétní požadavky, v tématu [Jak vytvořit rozšíření v daňové službě](./tax-service-add-data-fields-tax-integration-by-extension.md) najdete informace o tom, jak vygenerovat a vybrat vlastní daňovou konfiguraci.

14. Poté, co vyberete **Verzi konfigurace**, objeví se několik dalších karet. Dokončete povinné nastavení karty podle následujícího pořadí.

    **Povinné nastavení**

    - **Kódy daně** - k udržování kmenových dat pro daňové kódy. Všechny daňové kódy, které jsou vytvořeny na této kartě, se automaticky synchronizují do Finance, když povolíte aktuální verzi.
    - **Daňová skupina** - Definujte kmenová data daňové skupiny a daňové kódy v rámci skupiny.
    - **Daňová skupina zboží** - Definujte kmenová data daňové skupiny zboží a daňové kódy v rámci skupiny.

    **Volitelné nastavení**

    - **Použitelnost daňové skupiny** - Definujte matici, která určuje daňovou skupinu. Pokud žádná pravidla použitelnosti v této matici neodpovídají zdanitelnému dokladu z Dynamics 365, výpočet daně použije výchozí hodnotu na řádku zdanitelného dokladu.
    - **Použitelnost daňové skupiny zboží** - Definujte matici, která určuje daňovou skupinu zboží. Pokud žádná pravidla použitelnosti v této matici neodpovídají zdanitelnému dokladu z Dynamics 365, výpočet daně použije výchozí hodnotu na řádku zdanitelného dokladu.
    - **Použitelnost DIČ zákazníka** - Pokud máte více daňových registračních čísel pro jednoho zákazníka, může Výpočet daně automaticky určit správné daňové registrační číslo. V matici na této kartě definujete pravidla, která by se měla použít k určení. Jinak budou Finance a Supply Chain Management i nadále používat u prodejních transakcí výchozí daňové registrační číslo na zdanitelných dokladech.
    - **Použitelnost DIČ dodavatele** - Pokud máte více daňových registračních čísel pro jednoho dodavatele, může Výpočet daně automaticky určit správné daňové registrační číslo. V matici na této kartě definujete pravidla, která by se měla použít k určení. Jinak budou Finance a Supply Chain Management i nadále používat u nákupních transakcí výchozí daňové registrační číslo na zdanitelných dokladech.
    - **Použitelnost kódu seznamu** - automatické určení hodnoty pole **Kód seznamu** prostřednictvím flexibilnějších a konfigurovatelnějších pravidel. V matici na této kartě definujete pravidla, která by se měla použít k určení. Jinak budou Finance a Supply Chain Management i nadále používat u zdanitelných dokladů výchozí kód.

14. Na kartě **Daňové kódy** vyberte **Přidat** a zadejte daňový kód a popis.
15. Vyberte možnost **Daňová komponenta**. Daňová komponenta je skupina metod, které byly definovány v předchozí verzi vybrané daňové konfigurace. K dispozici jsou následující daňové komponenty:

    - Podle čisté částky
    - Podle hrubé částky
    - Podle množství
    - Podle marže
    - Daň z daně

16. Zvolte **Uložit**. Na základě vybrané daňové komponenty se zpřístupní více polí.
17. Pomocí následujících možností můžete určit povahu daňového kódu:

    - Je osvobozeno od daně
    - Je importní DPH
    - Je přenesení daňové povinnosti
    - Vyloučit z výpočtu základní částky

    Pro scénář importní DPH nastavte jeden daňový kód, který má kladnou sazbu daně, a označte jej jako **Je importní DPH**.

    Pro scénář přenesení daňové povinnosti nastavte dva daňové kódy, z nichž jeden má kladnou sazbu daně a druhý má zápornou sazbu daně, ale stejnou hodnotu sazby. Označte záporný daňový kód jako **Je přenesení daňové povinnosti**. Další informace o řešení přenesení daňové povinnosti ve Finance najdete v části [Mechanismus přenesení daňové povinnosti pro režim DPH / GST](emea-reverse-charge.md).

    U některých typů daní, které by měly být vyloučeny při výpočtu částky základu daně u transakcí zahrnujících cenu (např. celní sazba v některých zemích nebo regionech) vyberte zaškrtávací políčko **Vyloučit z výpočtu základní částky**. Další informace o tomto parametru naleznete v tématu [Výpočet daně navíc k ceně, když jsou povoleny Ceny včetně daní](global-exclude-from-tax-base-amount-calculation.md).

    Udržujte daňové sazby a limity výše daně pro tento daňový kód.

18. Opakujte kroky 14 až 17 pro všechny další povinné daňové kódy, které chcete přidat.
19. Na kartě **Daňová skupina** vyberte sloupec **Daňová skupina**, přidejte jej do matice jako vstupní podmínku a poté přidejte řádky pro zachování kmenových dat daňové skupiny.

    Následuje příklad.

    | Daňová skupina    | Kódy daně           |
    | ------------ | ------------------- |
    | DEU_Dom | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Dom | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. Na kartě **Daňová skupina zboží** vyberte sloupec **Daňová skupina zboží**, přidejte jej do matice jako vstupní podmínku a poté přidejte řádky pro zachování kmenových dat daňové skupiny zboží.

    Následuje příklad.

    | Skupina daně zboží | Kódy daně                                    |
    | -------------- | -------------------------------------------- |
    | Plný           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Výjimka |
    | Snížené        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. Na kartě **Použitelnost daňové skupiny** vyberte sloupce, které jsou nutné k určení správné daňové skupiny, a poté vyberte **Přidat**. Zadejte nebo vyberte hodnoty pro každý sloupec. Pole **Daňová skupina** bude výstupem této matice. Pokud tato karta není nakonfigurována, použije se skupina daně z prodeje na řádku transakce.

    Následuje příklad.

    | Obchodní proces | Odeslat z | Místo dodání | Daňová skupina    |
    | ---------------- | --------- | ------- | ------------ |
    | Prodej            | DEU       | DEU     | DEU_Dom |
    | Prodej            | DEU       | FRA     | DEU_EU       |
    | Prodej            | BEL       | BEL     | BEL_Dom |
    | Prodej            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Pokud je výchozí skupina daně z obratu na řádcích vašeho zdanitelného dokladu správná, ponechte tuto matici prázdnou. Více informací naleznete v části [Návrh runtime](#runtime) v dále v tomto článku.

22. Na kartě **Použitelnost daňové skupiny zboží** vyberte sloupce, které jsou nutné k určení správného daňového kódu, a poté vyberte **Přidat**. Zadejte nebo vyberte hodnoty pro každý sloupec. Pole **Daňová skupina zboží** bude výstupem této matice. Pokud tato karta není nakonfigurována, použije se skupina DPH zboží na řádku transakce.

    Následuje příklad.

    | Kód položky | Skupina daně položky |
    | --------- | -------------- |
    | D0001     | Celý           |
    | D0003     | Snížené        |

    > [!NOTE]
    > Pokud je výchozí skupina položek daně z obratu na řádcích vašeho zdanitelného dokladu správná, ponechte tuto matici prázdnou. Více informací naleznete v části [Návrh runtime](#runtime) v dále v tomto článku.

    Další informace o tom, jak se určují daňové kódy ve Výpočtu daně, viz [Logika určování skupiny DPH a skupiny DPH zboží](global-sales-tax-group-determination.md).

23. Nastavte použitelnost DIČ zákazníka, DIČ dodavatele a kódů seznamu dle obchodních potřeb.
24. Zvolte **Uložit** a pak zavřete stránku.
25. Vyberte **Změnit stav** \> **Dokončeno**. Po změně stavu na **Dokončeno** již verzi nelze upravovat.
26. Vyberte **Změnit stav** \> **Publikovat**. Tato verze nastavení funkce daně bude přenesena do globálního úložiště a bude viditelná pro každou právnickou osobu ve službě Finance.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Nastavení výpočtu daně v Dynamics 365

Po dokončení nastavení v RCS budete mít publikovanou verzi daňové funkce. Pomocí těchto kroků nastavíte výpočet daně ve Finance.

Nastavení v této části provádí právnická osoba. Musíte jej konfigurovat pro každou právnickou osobu, pro kterou chcete ve Finance aktivovat výpočet daně.

1. Ve Finance přejděte do nabídky **Daň** \> **Nastavení** \> **Daňová konfigurace** \> **Parametry výpočtu daně**.
2. Na kartě **Obecné** natavte následující pole:

    - **Povolit službu výpočtu daně** – Zaškrtnutím tohoto políčka povolíte výpočet daně pro právnickou osobu. Pokud není pro aktuální právnickou osobu povolen, bude právnická osoba i nadále k určení a výpočtu daně používat stávající daňový modul.
    - **Nastavení funkce** – Vyberte publikované nastavení a verzi daňové funkce pro právnickou osobu. Další informace o tom, jak nastavit a dokončit publikovanou daňovou funkci, najdete v předchozí části tohoto článku.
    - **Obchodní proces** – Vyberte obchodní procesy, které chcete povolit.

3. Na kartě **Výpočet** definujte očekávané pravidlo zaokrouhlování pro právnickou osobu. Další informace o logice zaokrouhlení viz [Pravidla zaokrouhlování výpočtu daně](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Na kartě **Zpracování chyb** definujte očekávanou metodu zpracování chyb pro právnickou osobu. K dispozici jsou tři možnosti:

    - Ne
    - Upozornění
    - Chyba

    V každém kódu výsledku můžete nastavit metodu zpracování chyb v sekci **Podrobnosti**. Alternativně, pokud některé kódy výsledků nejsou synchronizovány ze služby pro výpočet daně, můžete nastavit výchozí metodu v sekci **Všeobecné**.

5. Na kartě **Vícenásobná registrace DPH** můžete samostatně zapnout přiznání DPH, seznam prodejů v EU a Intrastat, aby fungovaly podle scénáře vícenásobné registrace DPH. Další informace o vykazování daní pro více registrací DPH naleznete v části [Hlášení pro více registrací DPH](emea-reporting-for-multiple-vat-registrations.md).
6. Uložte nastavení a opakujte předchozí kroky pro každou další právnickou osobu. Když je publikována nová verze a chcete, aby byla použita, nastavte pole **Nastavení funkcí** na kartě **Všeobecné** na stránce **Parametry výpočtu daně** (viz krok 2).
