---
title: Mechanismus přenesení daňové povinnosti pro režim DPH / GST
description: Toto téma popisuje určení přenesení daňové povinnosti (reverse charge) pro DPH u evropských zemí, v Saúdské Arábii a Singapuru.
author: epodkolz
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore, Bahrain, Kuwait, Oman, Qatar
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b9996b4d6ab84070cc3e9863a454c4fd8ed14091490273cde0eec1ea2bc508fc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756219"
---
# <a name="reverse-charge-mechanism-for-vatgst-scheme"></a>Mechanismus přenesení daňové povinnosti pro režim DPH / GST

[!include [banner](../includes/banner.md)]

Toto téma popisuje obecný přístup k nastavení funkce přenesení daňové povinnosti pro země / regiony, které přijímají režimy DPH nebo GST.
                                                                                 
Dostupnost funkce v zemi / oblasti je řízena následujícími funkcemi v pracovním prostoru **Správa funkcí**.

| Funkce                                              | Země nebo oblast                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Žádná konkrétní funkce                                | Rakousko </br>Belgie </br>Bulharsko </br>Chorvatsko </br>Kypr </br>Česká republika </br>Dánsko  </br>Estonsko  </br>Finsko  </br>Francie  </br>Německo  </br>Maďarsko  </br>Island  </br>Irsko  </br>Itálie  </br>Lotyšsko  </br>Lichtenštejnsko  </br>Litva  </br>Lucembursko  </br>Nizozemsko  </br>Norsko Polsko </br>Portugalsko </br>Rumunsko  </br>Saúdská Arábie </br>Singapur  </br>Slovensko  </br>Slovinsko  </br>Španělsko  </br>Švédsko  </br>Švýcarsko  </br>Spojené království  </br>Spojené arabské emiráty |
| Zpětný poplatek za další země            | Bahrajn  </br>Kuvajt  </br>Omán  </br>Katar                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Povolit mechanismus přenesení daňové povinnosti pro schéma DPH/GST | Všechny ostatní země / regiony kromě:  </br>Brazílie  </br>Indie  </br>Rusko                                                                                                                                                                                                                                                                                                                                                                                         |
 
 Další informace viz [Povolení mechanismu zpětného účtování pro funkci schématu DPH / GST](#enable-reverse-charge) dále v tomto tématu.

Mechanismus reverse charge znamená přenesení odpovědnosti za účetnictví a vykazování DPH z prodávajícího na kupujícího. Příjemce tedy do výkazu DPH uvádí DPH na výstupu (v roli prodávajícího) i DPH na vstupu (v roli kupujícího).

V některých zemích nebo regionech se tedy mechanismus reverse charge uplatňuje jen na některé druhy zboží nebo služeb a mohou platit další podmínky nebo prahové hodnoty pro částky prodeje. V jiných zemích nebo regionech závisí odpovědnost za placení DPH na statusu dodavatele a kupujícího. Pokud je kupující plátcem DPH, tato skutečnost musí být jasně uvedena na faktuře vydané dodavatelem. Faktura například musí obsahovat výraz „reverse charge“ (přenesení daňové povinnosti) a informace o tom, na co se tento mechanismus vztahuje. 

Abyste mohli mechanismus reverse charge použít, je třeba provést následující nastavení.

## <a name="set-up-sales-tax-codes"></a>Nastavit kódy DPH
Doporučujeme používat pro nákupní a prodejní operace samostatné kódy DPH.

<table>
<body>
<tr>
<td><strong>Kód DPH u prodeje</strong></td>
<td>Vytvořte kód daně z prodeje pro operace prodeje zpětného účtování (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Kódy daně z prodeje</strong>).
</td>
</tr>
<tr>
<td><strong>Kód DPH u nákupu</strong></td>
<td><p>Vytvořte kladné a záporné kódy DPH pro mechanismus reverse charge VAT pro nákupy (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Kódy daně z prodeje</strong>).</p>
<ol>
<li>Vytvořte kód DPH s kladnou hodnotou.</li>
<li>Vytvořte kód DPH se zápornou hodnotou. Nastavte možnost <strong>Povolit záporné procento DPH</strong> na <strong>Ano</strong>.
Skupině DPH položek je třeba přiřadit tento záporný kód DPH a pak přiřadit tuto skupinu DPH položkám, kterých se mechanismus reverse charge týká.</li>
</ol>
<p>Další informace najdete v následující části &quot;Nastavení skupin DPH a skupin DPH položek.&quot;</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><a name="sales-tax-item-sales-tax-groups"></a>Nastavení skupin DPH a skupin DPH položky
Doporučujeme používat pro nákupní a prodejní operace samostatné skupiny DPH.

<table>
<tr>
<td><strong>Skupiny DPH u prodeje</strong></td>
<td>Vytvořte skupinu DPH pro operace prodeje s nastavením reverse charge (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Skupiny daně z prodeje</strong>). Na kartě <strong>Nastavení</strong> přidejte do této skupiny kód DPH pro reverse charge. Zaškrtněte možnosti <strong>Osvobozené od daně</strong> a <strong>Stornovací poplatek</strong> u příslušného kódu.</td>
</tr>
<tr>
<td><strong>Skupiny DPH u nákupu</strong></td>
<td>Vytvořte skupinu DPH pro operace nákupu s nastavením reverse charge (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Skupiny daně z prodeje</strong>). Na kartě <strong>Nastavení</strong> přidejte do této skupiny kladný a záporný kód DPH. U kódu se zápornou hodnotou zaškrtněte políčko <strong>Stornovací poplatek</strong>.</td>
</tr>
<tr>
<td><strong>Skupiny DPH položky</strong></td>
<td>Vytvořte nebo aktualizujte skupinu DPH položky pomocí kódu DPH se zápornou hodnotou (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Skupiny daně z prodeje zboží</strong>). Výchozí skupinu DPH položky je třeba přiřadit k produktům a kategoriím, na které se mechanismus reverse charge vztahuje.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-item-groups"></a><a name="reverse-charge-item-group"></a>Nastavení skupin položek přenesení daňové povinnosti
Na stránce **Stornovací poplatek – skupiny položek** (**Daň** &gt; **Nastavení** &gt; **DPH** &gt; **Stornovací poplatek – skupiny položek**) je možné definovat skupiny produktů nebo služeb (případně jednotlivé produkty či služby), pro které má mechanismus reverse charge platit. U každé skupiny položek pro reverse charge definujte seznam položek, skupin položek a kategorií pro prodej nebo nákup.

## <a name="set-up-reverse-charge-rules"></a><a name="reverse-charge-rules"></a>Nastavení pravidel pro reverse charge
Na stránce **Pravidla pro stornovací poplatek** (**Daň** &gt; **Nastavení** &gt; **DPH** &gt; **Pravidla pro stornovací poplatek**) je možné definovat pravidla pro účely nákupu a prodeje. Je možné nakonfigurovat sadu pravidel pro platnost mechanismu reverse charge. U každého pravidla je třeba nastavit tato pole:

- **Typ dokumentu** – vyberte možnost **Nákupní objednávka**, **Deník faktur dodavatele**, **Prodejní objednávka**, **Volná faktura**, **Deník faktur odběratele** a/nebo **Faktura dodavatele**.
- **Typ země/oblasti partnera** – vyberte možnost **Domácí**, **EU**, **GCC** nebo **Zahraniční**. Pokud lze pravidlo použít pro všechny partnery (bez ohledu na zemi či oblast, kde se adresa nachází), vyberte možnost **Vše**.
- **Domácí adresa dodání** – zaškrtnutím tohoto políčka použijete pravidlo u dodávek ve stejné zemi nebo oblasti. U typů dokumentů **Deník faktur dodavatele** a **Deník faktur odběratele** nelze toto políčko zaškrtnout.
- **Stornovací poplatek – skupina položek** – vyberte skupinu, pro kterou má pravidlo platit.
- **Prahová částka** – mechanismus reverse charge se u faktury použije pouze v případě, že hodnota položek nebo služeb ve skupině překročí zde zadanou hodnotu.

Období platnosti pravidla lze také nastavit pomocí polí **Datum platnosti** a **Datum vypršení platnosti**.

Je také možné určit, zda se má zobrazit oznámení a zda se má a řádek dokumentu aktualizovat podle výchozí skupiny DPH pro reverse charge, pokud bude splněna příslušná podmínka. Existují tyto možnosti:

- **Žádné** – řádek dokumentu se neaktualizuje.
- **Výzva** – zobrazí se oznámení s potvrzením o použitelnosti mechanismu reverse charge.
- **Nastavit** – řádek dokumentu se aktualizuje bez oznámení.

## <a name="set-up-countryregion-properties"></a><a name="Set-up-Country/region-properties"></a>Nastavení vlastností země/oblasti
Na stránce **Parametry zahraničního obchodu** (**Daň** &gt; **Nastavení** &gt; **Prodejní daň** &gt; **Zahraniční obchod** &gt; **Parametry zahraničního obchodu**) na kartě **Vlastnosti země/oblasti** nastavte zemi/oblast aktuální právnické osoby na *Domácí*. Nastavte **Typ země/oblasti** zemí EU, které se účastní obchodu v rámci EU, s aktuální právnickou osobou na hodnotu *EU*. Nastavte **Typ země/oblasti** zemí GCC, které se účastní obchodu v rámci GCC, s aktuální právnickou osobou na hodnotu *GCC*.

## <a name="set-up-default-parameters"></a>Nastavení výchozích parametrů
Funkci reverse charge VAT aktivujete tak, že na stránce **Parametry hlavní knihy** na kartě **Stornovací poplatek** nastavíte možnost **Povolit stornovací poplatek** na **Ano**. V polích **Nákupní objednávka – skupina DPH** a **Prodejní objednávka – skupina DPH** vyberte výchozí skupiny DPH. Při splnění podmínky použitelnosti přenesení daňové povinnosti se u řádku nákupní nebo prodejní objednávky aktualizují tyto skupiny DPH.

## <a name="reverse-charge-on-a-sales-invoice"></a><a name="reverse-charge-sale"></a>Reverse charge u prodejní faktury
U prodeje s mechanismem reverse charge prodávající neúčtuje DPH. Místo toho jsou na faktuře uvedeny položky, na které se vztahuje reverse charge, a celková částka DPH pro reverse charge.

Při zaúčtování prodejní faktury s přenesením daňové povinnosti mají transakce DPH směr **DPH na výstupu** a nulové DPH a jsou zaškrtnuta políčka **Přenesení daňové povinnosti** a **Osvobození od daně**.

## <a name="reverse-charge-on-a-purchase-invoice"></a><a name="reverse-charge-purchase"></a>Reverse charge u nákupní faktury
U nákupů s mechanismem reverse charge funguje kupující, který přijímá fakturu s reverse charge, pro účely účetnictví DPH jako kupující i prodávající.

Při zaúčtování nákupní faktury s reverse charge se vytvoří dvě transakce DPH. Jedna transakce má směr **DPH na vstupu**. Druhá transakce má směr **DPH na výstupu** a je u ní zaškrtnuto políčko **Stornovací poplatek**.

Následující snímek obrazovky má jedna transakce směr **DPH na vstupu** směru a druhá **DPH na výstupu**. 

![Zaúčtování DPH.](media/apac-sau-posted-sales-tax.png)

## <a name="enable-reverse-charge-mechanism-for-vatgst-scheme-feature"></a><a name="enable-reverse-charge"></a>Povolit mechanismus přenesení daňové povinnosti pro funkci schématu DPH/GST
V pracovním prostoru **Správa funkcí** najděte funkci a vyberte **Povolit**.

Po povolení funkce bude karta **Zpětné náklady** dostupná u všech právnických osob. Povolte funkci stornovacího poplatku pro právnickou osobu nastavením možnosti **Povolit přenesení poplatků** na **Ano**.

K dispozici budou následující stránky a položky nabídky související s nastavením funkce:
 - **Skupiny položek stornovacího poplatku** (**Daň** > **Nastavení** > **DPH** > **Skupiny položek stornovacího poplatku**). Další informace naleznete v části [Nastavení skupin položek přenesení daňové povinnosti](#reverse-charge-item-group).
 - **Pravidla stornovacího poplatku** (**Daň** > **Nastavení** > **DPH** > **Pravidla stornovacího poplatku**). Viz [Nastavení pravidel stornovacího poplatku](#reverse-charge-rules).
 - **Parametry zahraničního obchodu** (**Daň** > **Nastavení** > **DPH** > **Zahraniční obchod** > **Parametry zahraničního obchodu**). Viz [Nastavení vlastností země/oblasti](#Set-up-Country/region-properties).

Zaškrtávací políčko **Stornovací poplatek** bude k dispozici na stránkách **Skupina DPH** a **Zaúčtovaná DPH**. Další informace najdete v částech [Nastavení skupin DPH a skupin DPH položek](#sales-tax-item-sales-tax-groups), [Stornovací poplatek na prodejní faktuře](#reverse-charge-sale) a [Stornovací poplatek na nákupní faktuře](#reverse-charge-purchase).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]