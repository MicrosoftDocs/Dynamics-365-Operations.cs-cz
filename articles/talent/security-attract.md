---
title: Správa rolí a zabezpečení v aplikaci Attract
description: Toto téma poskytuje informace o zabezpečení datových entit v Microsoft Dynamics 365 for Talent - Attract.
author: josaw1
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: josaw1
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5674df1657b46aa31e2011562f4ebbff2c16fee9
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2019
ms.locfileid: "374773"
---
# <a name="security-and-role-management-in-attract"></a>Správa rolí a zabezpečení v aplikaci Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract vyžaduje zabezpečení na základě rolí. Jinými slovy, přístup není udělován jednotlivým uživatelům, nýbrž rolím zabezpečení, ke kterým jsou uživatelé přiřazeni. Uživatel, který je přiřazen k roli zabezpečení, má přístup k sadě oprávnění, která je přidružena k této roli.

Attract poskytuje pět základních uživatelských rolí:

- Správce
- Náborový manažer
- Náborový pracovník
- Tazatel na pohovoru
- Pouze pro čtení

Role správce je jediná role, která má oprávnění k přidávání ostatních uživatelů a změnám jejich oprávnění.

- **Přidání** – V centru pro správu na kartě **Oprávnění uživatele** zvolte **Přiřadit role**, vyhledejte uživatele, kterého chcete přidat, a poté mu přiřaďte oprávnění.
- **Úprava** – Vyhledejte uživatele nebo hledejte uživatele v seznamu a poté vyberte **Upravit** pro změnu jeho oprávnění.
- **Odstranění** – Pokud odstraníte oprávnění určitého uživatele, neodeberete uživatele ze systému. Omezíte však uživatelům přístup a jeho oprávnění v aplikaci Attract. Například Hilda byla přiřazena k roli náborového manažera a je přidána k práci jako náborový manažer. Pokud je později Hilda odebrána z role náborového manažera, zůstává u práce jako náborový manažer a k této práci má stále přístup. Nemůže však vytvářet jiné práce.

Následující části poskytují stručný popis každé role. Tabulky dále v tomto tématu poskytují podrobnější informace.

> [!NOTE]
> Některé funkce jsou k dispozici pouze s doplňkem Komplexní nábor pro aplikaci Attract.

## <a name="administrator"></a>Správce

Uživatelé, kteří jsou přiřazeni k roli správce, mají přístup ke všem datům v aplikaci Attract a mohou je měnit. Správci mohou vytvářet, číst, aktualizovat a odstranit data. Mají také přístup do centra pro správu, kde mohou konfigurovat aplikaci Attract a nastavit informace o uživateli. Doporučujeme přiřadit alespoň jednu osobu k roli správce. Ve výchozím nastavení je správce prostředí v Microsoft PowerApps nastaven jako správce v aplikaci Attract. Pokud jste se přihlásili ke zkušební verzi aplikace Attract, role správce je vám automaticky přiřazena. V současné době pro vytváření prací musí mít uživatelé, kteří mají roli administrátora, také roli náborového pracovníka nebo náborového manažera.

## <a name="hiring-manager"></a>Náborový manažer

Uživatelé, kteří jsou přiřazeni k roli náborového manažera, mohou vytvářet práce a aktualizovat práce, které vytvořili dříve. Náboroví manažeři mohou provádět pouze omezené množství akcí u práce a žádostí, které jsou přidruženy k dané práci. Pouze uživatele, kteří jsou přiřazeni k roli náborového manažera, lze přidat do náborového týmu jako náborové manažery.

## <a name="recruiter-role"></a>Role náborového pracovníka

Uživatelé, kteří jsou přiřazeni k roli náborového pracovníka, mají úplná oprávnění ke čtení, vytváření, aktualizaci a odstranění prací, které vytvořili. Mají též úplná oprávnění ke čtení, vytváření, aktualizaci a odstranění aplikací, které jsou přiřazeny k pracím, které vlastní. Pouze uživatele, kteří jsou přiřazeni k roli náborového pracovníka, lze přidat do náborového týmu jako náborové pracovníky.

## <a name="interviewer"></a>Tazatel

Každý uživatel, který má účet Microsoft Azure Active Directory (Azure AD) v organizaci, může být přidán do náborového týmu jako tazatel na pohovoru. Uživatelé, kteří jsou přiřazeni k roli tazatele na pohovoru, mohou zobrazit podrobnosti o práci a data uchazeče pro práce, u kterých jsou členy náborového týmu. Pro tyto práce mohou tazatelé na pohovoru též činit náborová doporučení a poskytovat zpětnou vazbu o kandidátech. Nemohou však aktualizovat podrobnosti o práci nebo data uchazeče.

## <a name="read-only"></a>Pouze pro čtení

Uživatelé, kteří jsou přiřazeni k roli jen pro čtení, mají přístup pouze pro čtení ke všem datům v prostředí Attract. Nemohou však vytvářet nebo upravovat data.

## <a name="delegated-roles"></a>Delegované role

Pro každou práci, u níž jsou v náborovém týmu, mohou náboroví pracovníci a náboroví manažeři za sebe určit jednoho nebo více delegátů. Nemohou však určit delegáty pro jiné osoby v náborovém týmu.

Delegáti mají stejná oprávnění jako osoba, která je určila. Například pokud náborový manažer za sebe určí delegáta pro práci, delegát bude mít stejná oprávnění pro tuto práci jako náborový manažer. Delegáti nemohou odebrat jiné delegáty z náborového týmu. Nemohou ani odstranit osoby, které je určili jako delegáty.

## <a name="job-details-and-actions"></a>Podrobnosti o práci a akce

Uživatelé, kteří mají roli náborového manažera nebo náborového pracovníka, mohou vytvářet práce. Následující oprávnění se vztahují na podrobnosti o práci a akce, které lze u práce provádět.

| Data nebo akce    | Náborový pracovník | Náborový manažer | Tazatel na pohovoru |
|-------------------|-----------|----------------|-------------|
| Podrobnosti o práci       | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Pouze pro čtení |
| Náborový tým       | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Pouze pro čtení |
| Nabídka volných pracovních míst       | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Pouze pro čtení | Pouze pro čtení |
| Zpracovat           | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Pouze pro čtení |
| Přidání uchazečů    | Přidání uchazečů pro práce, u kterých je uživatel členem náborového týmu | Přidání uchazečů pro práce, u kterých je uživatel členem náborového týmu | Nepovoleno |
| Přidání potenciálních uchazečů     | Přidání potenciálních uchazečů pro práce, u kterých je uživatel členem náborového týmu | Možnost konfigurace v [nastavení aktivit potenciálního uchazeče](./activities-attract.md#prospect-activity) kontroluje, zda mohou tazatelé na pohovoru přidávat a zobrazovat potenciální uchazeče. | Nepovoleno |
| Aktivace práce      | Aktivace prací, u kterých je uživatel členem náborového týmu | Aktivace prací, u kterých je uživatel členem náborového týmu | Nepovoleno |
| Uzavřít práci         | Uzavření prací, u kterých je uživatel členem náborového týmu | Nepovoleno | Nepovoleno |
| Odstranit úlohu        | Odstranění prací, u kterých je uživatel členem náborového týmu | Pouze v případě, že žádní žadatelé nebyli přidáni k práci | Nepovoleno |
| Odstranit uchazeče | Odstranění žádostí, pokud je uživatel členem náborového týmu | Nepovoleno | Nepovoleno |

## <a name="application-details-and-actions"></a>Podrobnosti o žádosti a akce

Následující oprávnění se vztahují na data specifická pro práci u uchazečů a akce, které lze u žádostí provádět.

| Data nebo akce          | Náborový pracovník | Náborový manažer | Tazatel na pohovoru |
|-------------------------|-----------|----------------|-------------|
| Dokumenty žádosti   | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Pouze pro čtení |
| Poznámky k žádosti       | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Vytváření, čtení, aktualizace a odstranění u prací, u kterých je uživatel v náborovém týmu | Vytvořit |
| Aktivita žádosti    | Zobrazení, pokud je uživatel členem náborového týmu | Zobrazení, pokud je uživatel členem náborového týmu | Pouze pro čtení |
| Zpětná vazba k žádosti    | Přidání a zobrazení všech zpětných vazeb, pokud je uživatel členem náborového týmu | Přidání a zobrazení všech zpětných vazeb, pokud je uživatel členem náborového týmu | Může přidat zpětnou vazbu\*\* |
| Odmítnutí žádosti      | Může zamítnout, pokud je uživatel členem náborového týmu | Nepovoleno | Nepovoleno |
| Postoupit do další fáze           | Může zamítnout, pokud je uživatel členem náborového týmu | Může posunout dál, pokud je uživatel členem náborového týmu | Nepovoleno |
| Spuštění správy nabídek | Může spustit správu nabídek | Existuje možnost konfigurace pro aktivitu nabídky. | Nepovoleno |

\*\* Možnost konfigurace v [nastavení aktivity zpětné vazby](activities-attract.md#feedback-activity) kontroluje, zda mohou tazatelé na pohovoru zobrazit zpětnou vazbu jeden druhého.

## <a name="process-templates"></a>Šablony procesu

Následující oprávnění platí na šablony náborového procesu. Možnost členů týmu vytvořit a upravit šablony se konfiguruje v možnosti **Správa šablon** v centru pro správu. Je-li správa šablon zapnutá, náboroví pracovníci a náboroví manažeři mohou vytvářet a upravovat své vlastní šablony procesu. Je-li správa šablon vypnuta, pouze správci mohou vytvářet a upravovat šablony procesů. Následující tabulka předpokládá, že je správa šablon zapnuta.

| Data              | Náborový pracovník                                           | Náborový manažer                                      | Tazatel na pohovoru |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Šablony procesu | Úplná oprávnění pro šablony, které uživatel vytvoří | Úplná oprávnění pro šablony, které uživatel vytvoří | Bez přístupu   |

## <a name="email-and-email-templates"></a>E-mail a e-mailové šablony

Následující oprávnění se vztahují na e-mailové šablony a akce, které lze u e-mailů provádět. Pouze správci mohou vytvořit a upravit e-mailové šablony.

| Data nebo akce     | Náborový pracovník          | Náborový manažer     | Tazatel na pohovoru |
|--------------------|--------------------|--------------------|-------------|
| Šablony e-mailů    | Přístup pouze pro čtení   | Přístup pouze pro čtení   | Bez přístupu   |
| Odeslat e-mail         | Odeslání podle aktivity  | Odeslání podle aktivity  | Bez přístupu   |
| Úprava e-mailového obsahu | Úprava e-mailového obsahu | Úprava e-mailového obsahu | Bez přístupu   |

## <a name="talent-pools"></a>Skupiny talentů

Následující oprávnění se vztahují na skupiny talentů. Skupiny talentů jsou viditelné pouze osobám, které je vytvořily, pokud si tato nevybere, že je bude sdílet. Vyhledávání kandidátů lze použít k vyhledávání kandidátů, kteří nebyli přidáni do pojmenované skupiny.

| Data nebo akce   | Náborový pracovník                                       | Náborový manažer                                  | Tazatel na pohovoru |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Pojmenovaná skupina       | Úplná oprávnění pro skupiny, které uživatel vytvoří | Úplná oprávnění pro skupiny, které uživatel vytvoří | Bez přístupu   |
| Sdílení skupiny       | Pouze skupiny, které uživatel vytvoří                | Pouze skupiny, které uživatel vytvoří                | Bez přístupu   |
| Vyhledávání kandidátů | Možnosti úplného vyhledávání                        | Možnosti úplného vyhledávání                        | Bez přístupu   |

## <a name="candidates"></a>Kandidáti

Kandidáti jsou osoby, které byly přidány do skupiny talentů, ale nejsou přiřazeni k práci.

| Data                        | Náborový pracovník                        | Náborový manažer                   | Tazatel na pohovoru |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profil - podrobnosti o kandidátovi | Vytvoření, čtení, aktualizace a odstranění | Vytvoření, čtení, aktualizace a odstranění | Bez přístupu   |
| Dokumenty                   | Vytvoření, čtení, aktualizace a odstranění | Vytvoření, čtení, aktualizace a odstranění | Bez přístupu   |
