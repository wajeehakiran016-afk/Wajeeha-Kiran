# Wajeeha-Kiran
Mathematics and Computer Science graduate with a strong foundation in problem-solving and software development. Passionate about Odoo development, web apps, and educational technology. Skilled in Python, databases, and OOP concepts. Focused on building efficient, user-friendly, and scalable solutions for real-world problems.
from odoo import models, fields

class Student(models.Model):
    _name = 'student.student'
    _description = 'Student'

    name = fields.Char(string="Name", required=True)
    roll_no = fields.Char(string="Roll Number", required=True, unique=True)
    dob = fields.Date(string="Date of Birth")
    gender = fields.Selection([
        ('male', 'Male'),
        ('female', 'Female')
    ])
    class_id = fields.Many2one('school.class', string="Class")
    phone = fields.Char(string="Contact Number")
    address = fields.Text(string="Address")
    admission_date = fields.Date(string="Admission Date")
