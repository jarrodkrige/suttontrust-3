# Submission from Jessica Basra

> Team 3 · Role software-developer-1 · 2026-05-08 13:54

import { Card, CardContent } from "@/components/ui/card";
import { BarChart, Bar, XAxis, YAxis, Tooltip, Legend, ResponsiveContainer } from "recharts";

const costData = [
  { name: "London Uni", Tuition: 9535, Living: 15000, Bursaries: -2000 },
  { name: "Russell Group (Non-London)", Tuition: 9535, Living: 11000, Bursaries: -1800 },
  { name: "Post-92 Uni", Tuition: 9000, Living: 9500, Bursaries: -1600 },
];

export default function FundingTab() {
  return (
    <div className="grid gap-6 p-6">
      <Card className="rounded-2xl">
        <CardContent className="p-6">
          <h2 className="text-xl font-semibold">Costs</h2>
          <p className="mt-2 text-base">
            If you’re a home student in England, undergraduate tuition fees are capped at £9,535 per year. You don’t pay this upfront—Student Finance covers it through a tuition fee loan paid directly to your university.
          </p>
        </CardContent>
      </Card>

      <Card className="rounded-2xl">
        <CardContent className="p-6">
          <h2 className="text-xl font-semibold">Living Costs</h2>
          <p className="mt-2">
            Living costs depend heavily on location. London students typically face higher rent and transport costs, while students outside London spend less overall. Maintenance loans help with rent, food, travel, books, and everyday expenses.
          </p>
        </CardContent>
      </Card>

      <Card className="rounded-2xl">
        <CardContent className="p-6">
          <h2 className="text-xl font-semibold">Cost Comparison</h2>
          <div className="h-72 mt-4">
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
          <p className="mt-2 text-sm text-muted-foreground">
            Bursaries shown reduce overall costs. Actual support depends on household income and university.
          </p>
        </CardContent>
      </Card>

      <Card className="rounded-2xl">
        <CardContent className="p-6">
          <h2 className="text-xl font-semibold">Bursaries, Grants & Extra Support</h2>
          <ul className="list-disc pl-5 mt-2">
            <li>University bursaries for low-income and first-generation students (often £500–£2,000 per year)</li>
            <li>Maintenance loans (means-tested, higher amounts for students in London)</li>
            <li>Disabled Students’ Allowance (non-repayable)</li>
            <li>Care leaver, estranged student, and commuter support funds</li>
            <li>Part-time work and paid internships during study</li>
          </ul>
        </CardContent>
      </Card>
    </div>
  );
}