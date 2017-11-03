---
title: "DPH stornovacího poplatku"
description: "Toto téma popisuje určení přenesení daňové povinnosti (reverse charge) pro DPH u evropských zemí."
author: epodkolz
manager: AnnBe
ms.date: 05/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dba651b4e6f0e661d6743780495c7ee217eefd9d
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="reverse-charge-vat"></a>DPH stornovacího poplatku
Toto téma popisuje obecný postup pro určení přenesení daňové povinnosti (reverse charge) pro DPH u evropských zemí.

Mechanismus reverse charge znamená přenesení odpovědnosti za účetnictví a vykazování DPH z prodávajícího na kupujícího. Příjemce tedy do výkazu DPH uvádí DPH na výstupu (v roli prodávajícího) i DPH na vstupu (v roli kupujícího).

Směrnice Evropské unie (EU) umožňují členským státům určit konkrétní adaptaci obecných požadavků v místním prostředí. V některých zemích se tedy mechanismus reverse charge uplatňuje jen na některé druhy zboží nebo služeb a mohou platit další podmínky nebo prahové hodnoty pro částky prodeje. V jiných zemích závisí odpovědnost za placení DPH na statusu dodavatele a kupujícího. Pokud je kupující plátcem DPH, tato skutečnost musí být jasně uvedena na faktuře vydané dodavatelem. Faktura například musí obsahovat výraz „reverse charge“ (přenesení daňové povinnosti) a informace o tom, na co se tento mechanismus vztahuje. 

Abyste mohli mechanismus reverse charge použít, je třeba provést následující nastavení.

## <a name="set-up-sales-tax-codes"></a>Nastavení kódů DPH
Doporučujeme používat pro nákupní a prodejní operace samostatné kódy DPH.

<table>
<body>
<tr>
<td><strong>Kód DPH u prodeje</strong></td>
<td>Vytvořte kód daně z prodeje pro operace prodeje zpětného účtování (<strong>Daň</strong> > <strong>Nepřímé daně</strong> > <strong>Daň z prodeje</strong> > <strong>Kódy daně z prodeje</strong>).
</td>
</tr>
<tr>
<td><strong>Kód DPH u nákupu</strong></td>
<td><p>Vytvořte kladné a záporné kódy DPH pro mechanismus reverse charge VAT pro nákupy (<strong>Daň</strong> > <strong>Nepřímé daně</strong> > <strong>Daň z prodeje</strong> > <strong>Kódy daně z prodeje</strong>).</p>
<ol>
<li>Vytvořte kód DPH s kladnou hodnotou.</li>
<li>Vytvořte kód DPH se zápornou hodnotou. Nastavte možnost <strong>Povolit záporné procento DPH</strong> na <strong>Ano</strong>.
Skupině DPH položek je třeba přiřadit tento záporný kód DPH a pak přiřadit tuto skupinu DPH položkám, kterých se mechanismus reverse charge týká.</li>
</ol>
<p>Další informace najdete v následující části Nastavení skupin DPH a skupin DPH položek.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Nastavení skupin DPH a skupin DPH položky
Doporučujeme používat pro nákupní a prodejní operace samostatné skupiny DPH.

<table>
<tr>
<td><strong>Skupiny DPH u prodeje</strong></td>
<td>Vytvořte skupinu DPH pro operace prodeje s nastavením reverse charge (<strong>Daň</strong> > <strong>Nepřímé daně</strong> > <strong>Daň z prodeje</strong> > <strong>Skupiny daně z prodeje</strong>). Na kartě <strong>Nastavení</strong> přidejte do této skupiny kód DPH pro reverse charge. Zaškrtněte možnosti <strong>Osvobozené od daně</strong> a <strong>Stornovací poplatek</strong> u příslušného kódu.</td>
</tr>
<tr>
<td><strong>Skupiny DPH u nákupu</strong></td>
<td>Vytvořte skupinu DPH pro operace nákupu s nastavením reverse charge (<strong>Daň</strong> > <strong>Nepřímé daně</strong> > <strong>Daň z prodeje</strong> > <strong>Skupiny daně z prodeje</strong>). Na kartě <strong>Nastavení</strong> přidejte do této skupiny kladný a záporný kód DPH. U kódu se zápornou hodnotou zaškrtněte políčko <strong>Stornovací poplatek</strong>.</td>
</tr>
<tr>
<td><strong>Skupiny DPH položky</strong></td>
<td>Vytvořte nebo aktualizujte skupinu DPH položky pomocí kódu DPH se zápornou hodnotou(<strong>Daň</strong> > <strong>Nepřímé daně</strong> > <strong>Daň z prodeje</strong> > <strong>Skupiny daně z prodeje zboží</strong>). Výchozí skupinu DPH položky je třeba přiřadit k produktům a kategoriím, na které se mechanismus reverse charge vztahuje.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a>Nastavení skupin pro reverse charge
Na stránce **Stornovací poplatek – skupiny položek** (**Daň** > **Nastavení** > **DPH** > **Stornovací poplatek – skupiny položek**) je možné definovat skupiny produktů nebo služeb (případně jednotlivé produkty či služby), pro které má mechanismus reverse charge platit. U každé skupiny položek pro reverse charge definujte seznam položek, skupin položek a kategorií pro prodej nebo nákup.

## <a name="set-up-reverse-charge-rules"></a>Nastavení pravidel pro reverse charge
Na stránce **Pravidla pro stornovací poplatek** (**Daň** > **Nastavení** > **DPH** > **Pravidla pro stornovací poplatek**) je možné definovat pravidla pro účely nákupu a prodeje. Je možné nakonfigurovat sadu pravidel pro platnost mechanismu reverse charge. U každého pravidla je třeba nastavit tato pole:

- **Typ dokumentu** – vyberte možnost **Nákupní objednávka**, **Deník faktur dodavatele**, **Prodejní objednávka**, **Volná faktura**, **Deník faktur odběratele** a/nebo **Faktura dodavatele**.
- **Typ země/oblasti partnera** – vyberte možnost **Domácí**, **EU** nebo **Cizí**. Pokud lze pravidlo použít pro všechny partnery (bez ohledu na zemi či oblast, kde se adresa nachází), vyberte možnost **Vše**.
- **Domácí adresa dodání** – zaškrtnutím tohoto políčka použijete pravidlo u dodávek ve stejné zemi nebo oblasti. U typů dokumentů **Deník faktur dodavatele** a **Deník faktur odběratele** nelze toto políčko zaškrtnout.
- **Stornovací poplatek – skupina položek** – vyberte skupinu, pro kterou má pravidlo platit.
- **Prahová částka** – mechanismus reverse charge se u faktury použije pouze v případě, že hodnota položek nebo služeb ve skupině překročí zde zadanou hodnotu.

Období platnosti pravidla lze nastavit pomocí polí **Datum platnosti** a **Datum vypršení platnosti**.

Je také možné určit, zda se má zobrazit oznámení a zda se má a řádek dokumentu aktualizovat podle výchozí skupiny DPH pro reverse charge, pokud bude splněna příslušná podmínka. Existují tyto možnosti:

- **Žádné** – řádek dokumentu se neaktualizuje.
- **Výzva** – zobrazí se oznámení s potvrzením o použitelnosti mechanismu reverse charge.
- **Nastavit** – řádek dokumentu se aktualizuje bez oznámení.

## <a name="set-up-default-parameters"></a>Nastavení výchozích parametrů
Funkci aktivujete tak, že na stránce **Parametry hlavní knihy** na kartě **Stornovací poplatek** nastavíte možnost **Povolit stornovací poplatek** na **Ano**. V polích **Nákupní objednávka – skupina DPH** a **Prodejní objednávka – skupina DPH** vyberte výchozí skupiny DPH. Při splnění podmínky použitelnosti přenesení daňové povinnosti se u řádku nákupní nebo prodejní objednávky aktualizují tyto skupiny DPH.

## <a name="reverse-charge-on-a-sales-invoice"></a>Reverse charge u prodejní faktury
U prodeje s mechanismem reverse charge prodávající neúčtuje DPH. Místo toho jsou na faktuře uvedeny položky, na které se vztahuje reverse charge, a celková částka DPH pro reverse charge.

Při zaúčtování prodejní faktury s reverse charge mají transakce DPH směr **DPH na výstupu** a nulové DPH a je zaškrtnuto políčko **Stornovací poplatek**.

## <a name="reverse-charge-on-a-purchase-invoice"></a>Reverse charge u nákupní faktury
U nákupů s mechanismem reverse charge funguje kupující, který přijímá fakturu s reverse charge, pro účely účetnictví DPH jako kupující i prodávající.

Při zaúčtování nákupní faktury s reverse charge se vytvoří dvě transakce DPH. Jedna transakce má směr **DPH na vstupu**. Druhá transakce má směr **DPH na výstupu** a je u ní zaškrtnuto políčko **Stornovací poplatek**.

