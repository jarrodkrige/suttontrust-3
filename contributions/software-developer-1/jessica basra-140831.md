# Submission from Jessica Basra

> Team 3 · Role software-developer-1 · 2026-05-08 14:08

Here is css for the funding section, make sure to include the graphs on the main pageimport { Card, CardContent } from "@/components/ui/card";
import { BarChart, Bar, XAxis, YAxis, Tooltip, Legend, ResponsiveContainer } from "recharts";

// Main page version of funding content (no tab dependency)
const costData = [
  { name: "London Uni", Tuition: 9535, Living: 15000, Bursaries: -2000 },
  { name: "Russell Group (Non-London)", Tuition: 9535, Living: 11000, Bursaries: -1800 },
  { name: "Post-92 Uni", Tuition: 9000, Living: 9500, Bursaries: -1600 },
];

export default function FundingMainSection() {
  return (
    <section className="max-w-6xl mx-auto p-6 space-y-10">
      {/* Page intro */}
      <header className="space-y-2">
        <h1 className="text-3xl font-bold">Funding Your Degree</h1>
        <p className="text-base text-muted-foreground">
          Money shouldn’t be a barrier to university. Here’s a clear breakdown of costs, support available, and how to budget as a first‑generation student.
        </p>
      </header>


      {/* Costs */}
      <Card className="rounded-2xl">
        <CardContent className="p-6 space-y-2">
          <h2 className="text-xl font-semibold">Tuition Fees (Home Students)</h2>
          <p>
            For home students in England, undergraduate tuition fees are capped at £9,535 per year. You don’t pay this upfront — a tuition fee loan from Student Finance England is paid directly to your university.
          </p>
        </CardContent>
      </Card>

      {/* Living costs */}
      <Card className="rounded-2xl">
        <CardContent className="p-6 space-y-2">
          <h2 className="text-xl font-semibold">Living Costs</h2>
          <p>
            Living costs include rent, food, travel, bills, books, and everyday spending. These vary a lot by location — London is significantly more expensive than most other cities.
          </p>
        </CardContent>
      </Card>

      {/* Maintenance loan */}
      <Card className="rounded-2xl">
        <CardContent className="p-6 space-y-3">
          <h2 className="text-xl font-semibold">Maintenance Loan</h2>
          <p>
            The maintenance loan helps cover living costs and is paid directly into your bank account in three termly instalments. The amount is means‑tested based on household income and where you live.
          </p>
          <ul className="list-disc pl-5">
            <li>Living with parents: up to ~£8,900 per year</li>
            <li>Living away from home (outside London): up to ~£10,500 per year</li>
            <li>Living away from home (in London): up to ~£13,700 per year</li>
          </ul>
          <p className="text-sm text-muted-foreground">
            You usually receive the maximum amount if household income is around £25,000 or below.
          </p>
        </CardContent>
      </Card>

      {/* Comparison chart */}
      <Card className="rounded-2xl">
        <CardContent className="p-6 space-y-4">
          <h2 className="text-xl font-semibold">Cost Comparison by University Type</h2>
          <div className="h-80">
            <ResponsiveContainer width="100%" height="100%">
              <BarChart data={costData}>
                <XAxis dataKey="name" />
                <YAxis />
                <Tooltip />
                <Legend />
                <Bar dataKey="Tuition" fill="#6366f1" />
                <Bar dataKey="Living" fill="#22c55e" />
                <Bar dataKey="Bursaries" fill="#f97316" />
              </BarChart>
            </ResponsiveContainer>
          </div>
          <p className="text-sm text-muted-foreground">
            Bursaries reduce overall costs. Amounts vary by university and household income.
          </p>
        </CardContent>
      </Card>

      {/* Bursaries */}
      <Card className="rounded-2xl">
        <CardContent className="p-6 space-y-2">
          <h2 className="text-xl font-semibold">Bursaries, Grants & Extra Support</h2>
          <ul className="list