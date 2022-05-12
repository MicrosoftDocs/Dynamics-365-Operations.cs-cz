---
title: Nastavení hodnot parametrů výpočtu nákladů
description: Když nastavujete modul Náklady za doručení, můžete definovat několik sad společných hodnot, které budou k dispozici, když vyberete konkrétní typy hodnot parametrů výpočtu nákladů v jiných částech aplikace. Toto téma vysvětluje postup nastavení těchto sad hodnot.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 335bed49b05bf64547d7ded885f365a30487484f
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644631"
---
# <a name="costing-parameter-values-setup"></a>Nastavení hodnot parametrů výpočtu nákladů

[!include [banner](../../includes/banner.md)]

Když nastavujete modul **Náklady za doručení**, můžete definovat několik sad společných hodnot a souvisejících nastavení pro každou hodnotu. Tyto hodnoty pak budou k dispozici, když vyberete konkrétní typy hodnot parametrů výpočtu nákladů v jiných částech aplikace. Toto téma vysvětluje postup nastavení těchto sad hodnot.

## <a name="set-up-cost-type-codes"></a>Nastavení kódů typů nákladů

Kódy typů nákladů určují typ nákladů, které vzniknou při vyložení zboží do skladu, nebo náklady cesty za doručení. I když obvykle zvyšují hodnotu zboží, lze je použít také k rozlišení částek zapisovaných do hlavní knihy. Úpravy hlavní knihy se používají, když se náklady se časově rozlišují, nebo během řady cest a posunu v jedné transakci.

> [!NOTE]
> Pokud je tabulka typů nákladů sdílena mezi právnickými osobami, musí být účtová osnova také sdílena mezi právnickými osobami. Jinak nebudou transakce zaúčtování fungovat správně.

Chcete-li nastavit kódy typů nákladů, přejděte na stránku **Náklady za doručení \> Nastavení výpočtu nákladů \> Kódy typů nákladů**. Pomocí tlačítek v podokně akcí můžete vytvářet nové kódy typů nákladů, upravovat stávající kódy nebo odstranit vybraný typ nákladů.

V následující tabulce jsou popsána pole, která jsou k dispozici pro každý typ nákladu.

| Pole | popis |
|---|---|
| Kód typu nákladů | Zadejte název kódu typu nákladů. |
| popis | Zadejte popis kódu typu nákladů. |
| Použijte přepravní sazbu | Tuto možnost nastavte na *Ano* pokud pro výpočet hodnoty těchto nákladů musí být použit směnný kurz cesty (někdy označovaný jako manažerský kurz). V takovém případě bude pro faktury v cizí měně namísto standardního výchozího nebo spotového směnného kurzu použit sazba za přepravu. |
| Kategorie vykazování | Toto pole stanoví kategorii vykazování pro typ nákladů. Sestavy lze tisknout buď podle kategorií vykazování, nebo podle typu nákladů. |
| Typ strany MD | Vyberte, zda má typ nákladů být připsán položce, na účet hlavní knihy nebo dodavateli. |
| Účtování strany MD | Pokud je pole **Typ debetu** nastaveno na *Účet hlavní knihy*, vyberte popis účtování. |
| MD účet | Pokud je pole **Typ debetu** nastaveno na *Účet hlavní knihy*, vyberte účet hlavní knihy, který bude použit. |
| Typ strany Dal | Vyberte, zda má tento typ nákladů být připsán ve prospěch položky, účtu hlavní knihy nebo dodavatele. |
| Účtování strany Dal | Pokud je pole **Typ kreditu** nastaveno na *Účet hlavní knihy*, vyberte popis účtování. |
| Dal účet | Pokud je pole **Typ kreditu** nastaveno na *Účet hlavní knihy*, vyberte účet hlavní knihy, který bude použit. |
| Clearingový účet | Vyberte clearingový účet pro typ nákladů. Doporučujeme zadat samostatný clearingový účet pro každý typ nákladů, aby vám pomohl s odsouhlasením. |
| Standardní typ zaúčtování nákladů | Pokud používáte standardní kalkulaci, vyberte popis zaúčtování. |
| Účet standardní odchylky nákladů | <p>Pokud používáte standardní kalkulaci, použije se k zaúčtování jakékoli odchylky účet, který je zde uveden. Tento účet používá rozdělení nákladů za doručení na stránce **Ceny položky**. Toto rozdělení je vytvořeno pomocí periodické rutiny pro aktualizaci cen.</p><p>Například standardní náklad položky je 15,00 USD, FOB je 13,00 USD a přepravné je 2,00 USD. Když je přijata faktura za zboží, položka je přijata za cenu 15,00 USD, ale u položky existuje standardní cenová odchylka 2,00 USD, protože skutečný FOB je 13,00 USD. Tato odchylka se zaúčtuje na účet standardní odchylky ceny, který je nastaven v profilu účtování položek. Protože odhadované přepravné je 2,00 USD, při zaúčtování skladové faktury není žádná odchylka. Když je však přijata faktura za přepravné, přepravné je 2,50 USD za jednotku. Proto se odchylka 0,50 USD zaúčtuje na zadaný náklad. |
| Účet odchylky klouzavého průměrného | <p>Pokud používáte kalkulaci klouzavého průměru, použije se k zaúčtování jakékoli odchylky účet, který je zde uveden.</p><p>Například odhadované přepravné je 2,00 USD. Když je však přijata faktura za přepravné, přepravné je 2,50 USD za jednotku. Proto musí být zaúčtována odchylka 0,50 USD.</p><p>Když je možnost **Zaúčtovat úpravy jako odchylku** nastavena na stránce **Parametry nákladů za doručení** na *Ano*, budou všechny odchylky mezi odhadovanými a skutečnými náklady na dopravu zaúčtovány na účet odchylky klouzavého průměru, který je zde uveden. Když je možnost **Zaúčtovat úpravy jako odchylku** nastavena na *Ne*, použije se standardní funkce a odchylka se použije buď na zásoby, nebo na účet odchylky klouzavého průměru, který je zde uveden, a to podle množství na skladě.</p> |
| Úvěrový akruální účet | Vyberte účet, který se použije k rozlišení odhadů nákladů při zaúčtování nákupní faktury. Toto pole se používá pouze v případě, kdy je možnost **Použít úvěrový akruální účet typu nákladů** nastavena na *Ano* na záložce **Kalkulace** na kartě **Všeobecné** stránky **Parametry nákladů za doručení**. |
| Úvěrový účet | Vyberte účet, který se používá k zachycení nákladů na příchozí dopravu, které byly fakturovány dodavatelem. Částka je zaúčtována jako debet. Protiúčet je účet odchylky zásob. Tato zaúčtování se používá pouze v případě, kdy je možnost **Zaúčtovat na účet poplatků v hlavní knize** na stránce **Parametry závazků** nastavena na *Ano*. |
| Účet odchylky | Účet, který bude použit jako protiúčet časového rozlišení poplatků při zaúčtování nákupní faktury. Toto pole se používá pouze v případě, kdy je možnost **Použít úvěrový akruální účet typu nákladů** nastavena na *Ano* na záložce **Kalkulace** na kartě **Všeobecné** stránky **Parametry nákladů za doručení**. |

## <a name="vendor-cost-type-groups"></a>Skupiny typu nákladů dodavatele

Skupiny typů nákladů na dodavatele pomáhají určit, jak jsou zjištěny poplatky *automatických nákladů* a použity na cestu. Dodavatelé, kteří mají podobné importní náklady, jsou navzájem propojeni. Například všichni dodavatelé z rozvíjejících se trhů platí stejné procento cla za stejný typ produktu, který je zakoupen na zavedeném trhu.

Skupiny typů nákladů dodavatele můžete spravovat na stránce **Náklady za doručení \> Nastavení výpočtu nákladů \> Skupiny typů nákladů dodavatele**. Stránka **Skupiny typů nákladů dodavatele** poskytuje mřížku se seznamem všech existujících skupin typů nákladů dodavatele. Pomocí tlačítek na panelu akcí můžete přidávat, odebírat a upravovat řádky v mřížce.

V následující tabulce jsou popsána pole, která jsou k dispozici v každém řádku mřížky.

| Pole | popis |
|---|---|
| Skupiny typu nákladů dodavatele | Zadejte jedinečný název pro skupinu typů nákladů dodavatele (například *Rozvíjející se trhy*). |
| popis | Zadejte popis skupiny typů nákladů dodavatele. Tento popis může poskytnout podrobnosti o úrovni nebo typu poplatku, který je spojen se skupinou prodejců. |

## <a name="item-cost-type-groups"></a>Skupiny typu nákladů položky

Skupiny typů nákladů položky pomáhají určit, jak jsou zjištěny poplatky *automatických nákladů* a použity na cestu. Obdobné položky jsou vzájemně propojeny. Například všechny položky, které mají celní sazbu 5 procent, mohou patřit do konkrétní skupiny typů nákladů.

Skupiny typů nákladů položky můžete spravovat na stránce **Náklady za doručení \> Nastavení výpočtu nákladů \> Skupiny typů nákladů položky**. Stránka **Skupiny typů nákladů položky** poskytuje mřížku se seznamem všech existujících skupin typů nákladů položky. Pomocí tlačítek na panelu akcí můžete přidávat, odebírat a upravovat řádky v mřížce.

V následující tabulce jsou popsána pole, která jsou k dispozici v každém řádku mřížky.

| Pole | popis |
|---|---|
| Skupiny typu nákladů položky | Zadejte jedinečný název pro skupinu typů nákladů položky (například *Clo 5 %*). |
| popis | Zadejte popis skupiny typů nákladů položky. Tento popis může poskytnout podrobnosti o úrovni nebo typu poplatku, který je spojen se skupinou položek. |

> [!NOTE]
> Typ nákladů položky je propojen s položkou prostřednictvím pole **Skupina typů nákladů** na záložce **Nákup** stránky položky **Uvolněný produkt**.

## <a name="transfer-order-cost-type-groups"></a>Skupiny typů nákladů převodního příkazu

Skupiny typů nákladů převodního příkazu pomáhají určit, jak jsou zjištěny poplatky *automatických nákladů*. Obdobné položky jsou vzájemně propojeny. Například všechny položky, které mají celní sazbu 7 procent, mohou patřit do konkrétní skupiny typů nákladů.

Skupiny typů nákladů převodního příkazu můžete spravovat na stránce **Náklady za doručení \> Nastavení výpočtu nákladů \> Skupiny typů nákladů převodního příkazu**. Stránka **Skupiny typů nákladů převodního příkazu** poskytuje mřížku se seznamem všech existujících skupin typů nákladů převodního příkazu. Pomocí tlačítek na panelu akcí můžete přidávat, odebírat a upravovat řádky v mřížce.

V následující tabulce jsou popsána nastavení, která jsou k dispozici v každém řádku mřížky.

| Pole | popis |
|---|---|
| Skupiny typů nákladů převodního příkazu | Zadejte jedinečný název pro skupinu typů nákladů převodního příkazu (například *Clo 7 %*). |
| popis | Zadejte popis skupiny typů nákladů převodního příkazu. Tento popis může poskytnout podrobnosti o úrovni nebo typu poplatku, který je spojen se skupinou typů nákladů převodního příkazu. |

> [!NOTE]
> Typ nákladů převodního příkazu je propojen s položkou prostřednictvím pole **Skupina nákladů převodního příkazu** na záložce **Nákup** stránky položky **Uvolněný produkt**.

## <a name="cost-templates"></a>Šablony nákladů

Pomocí šablon nákladů nastavíte výchozí hodnoty nastavení, která uživatelé, kteří získávají odhad nákladů, možná neznají. Šablony nákladů mohou pomoci snížit složitost procesu odhadu minimalizací výběrů, které musí uživatelé provést, aby získali přesný odhad.

Chcete-li pracovat s šablonami nákladů, přejděte na stránku **Náklady za doručení \> Nastavení kalkulace \> Šablony nákladů**. Na stránce **Šablony nákladů** se v podokně seznamu vlevo zobrazí všechny aktuální šablony nákladů. Pomocí tlačítek na panelu akcí můžete přidávat, odebírat a upravovat šablony.

V následující tabulce jsou popsána nastavení, která jsou k dispozici pro každou šablonu.

| Pole | popis |
|---|---|
| Šablona nákladů | Zadejte jedinečný název pro šablonu nákladů. Název obvykle popisuje koeficient faktorů nebo nákladů pro šablonu. |
| popis | Zadejte popis šablony nákladů. |
| Dopravní společnost | Vyberte účet dodavatele přepravní společnosti, který chcete přidružit k šabloně nákladů. |
| Způsob dodání | Vyberte způsob doručení, který má šablona nákladů použít při výpočtu odhadované ceny položky. Toto pole pomůže při odhadu nákladů určit automatické náklady spojené se zbožím. |
| Typ přepravního kontejneru | Vyberte typ přepravního kontejneru, který chcete přidružit k šabloně nákladů. Toto pole pomůže při odhadu nákladů určit automatické náklady spojené se zbožím. |
| Celní deklarant | Vyberte celního makléře (dodavatele), kterého chcete přidružit k šabloně nákladů. Toto pole pomůže určit automatické náklady spojené s odhadem nákladů. |
| Koeficient | Zadejte faktor, který se použije na konečný odhad nákladů na zboží. Chcete-li například přidat 10 procent k vypočítanému odhadu nákladů, zadejte *1,10*. |

## <a name="volumetric-divisors"></a>Objemové dělitele

Pro výpočet objemové hmotnosti se používají objemové dělitele. Každá přepravní / nákladní společnost formuluje své vlastní objemové dělitele. Dělitelé společnosti se navíc obvykle liší v závislosti na způsobu doručení. Například přeprava vzduchem a po moři mají často velmi odlišné dělitele. Společnost může také vytvářet složitější pravidla podle toho, odkud odesílá. Systém používá k nalezení objemové hmotnosti následující vzorec: Objemová hmotnost = Objem ÷ Objemový dělitel.

Například balíček odeslaný letecky má objem 3 krychlové metry (m³). Společnost ho zpoplatňuje na základě objemové hmotnosti a uplatňuje objemový dělitel 6. Tento dělitel vydělí objem a určí se tak objemová hmotnost. Proto je objemová hmotnost pro tento příklad 3 ÷ 6 = 0,5 kilogramu (kg).

Chcete-li nastavit objemové dělitele, přejděte na stránku **Náklady za doručení \> Nastavení výpočtu nákladů \> Objemové dělitele**. Stránka **Objemové dělitele** poskytuje mřížku se seznamem všech existujících objemových dělitelů. Pomocí tlačítek na panelu akcí můžete přidávat, odebírat a upravovat řádky v mřížce.

V následující tabulce jsou popsána pole, která jsou k dispozici v každém řádku mřížky.

| Pole | popis |
|---|---|
| Dopravní společnost | Vyberte účet dodavatele přepravní společnosti, který je spojen s objemovým dělitelem. |
| Kód typu nákladů | Vyberte kód typu nákladů, který je spojen s objemovým dělitelem. Toto pole slouží k vložení typů nákladů do intervalů sestav. Sestavy lze tisknout buď podle kategorií vykazování, nebo podle typu nákladů. |
| Výchozí přístav | Vyberte přístav „od“, na který se vztahuje objemový dělitel. |
| Objemový dělitel | Zadejte hodnotu objemového dělitele, která se použije na řádek. Hodnota každého balení bude vynásobena objemem, který zadáte, a vypočítá se tak objemová hmotnost daného balení. |

> [!NOTE]
> Systém použije maximální hodnotu údajů **skutečná hmotnost** a **objemová hmotnost**.
